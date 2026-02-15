## 🍳🥘🍲 College-Trend 🍲🥘🍳
- The bar chart displayed previously is quite good. However, the information it contains has not yet been explored in detail. For example, what if we want to see the trend in the number of students for each faculty from year to year.
- Alumni Career Path Integration: Linking historical enrollment data with the career outcomes of graduates provides a powerful recruitment tool for prospective students. If a specific "hybrid" major shows a 95% employment rate within six months, the university can lean into that data for marketing. This creates a feedback loop where market demand directly informs the expansion of specific academic departments.
- Financial Aid and Enrollment Synergy: Mapping the distribution of scholarships and grants against enrollment spikes helps determine the true ROI of financial incentives. It allows the university to see if an increase in a specific faculty's population is driven by academic reputation or by more aggressive financial aid packages. Understanding this balance is key to maintaining a sustainable budget while attracting top-tier talent.
- Retention and Attrition Correlation: Tracking the flow of students from freshman year to graduation within specific faculties reveals where students are most likely to drop out or switch majors. By identifying these "leakage points," departments can implement targeted academic support or mentorship programs to improve overall completion rates. This longitudinal view ensures that high enrollment numbers actually translate into successful alumni.
- Comparing the percentage of students in each faculty helps identify which departments are expanding the fastest. This allows the university to allocate resources and staff more effectively based on demand.
- Analyzing the ratio of male to female students within specific faculties can highlight progress in diversity and inclusion. These insights are essential for creating targeted recruitment strategies for underrepresented groups.
- Breaking down enrollment by the students' home regions can reveal the university's geographic reach and brand reputation. This data is invaluable for marketing teams looking to expand into new provinces or international markets.
- As modern careers evolve, students are increasingly drawn to programs that cross traditional faculty boundaries. Visualizing the rise of these hybrid majors can help the university design more relevant, future-proof curricula.
- External factors, such as changes in government funding or accreditation standards, often influence enrollment spikes or drops. Mapping these external events against your trend lines can explain sudden shifts in the data.
- Tracking student cohorts over time shows the specific years where students are most likely to leave the university. Identifying these "leakage points" per faculty is the first step toward improving student persistence.
- Linking enrollment numbers with graduation data per faculty reveals which departments are most successful at retaining students. If a high-growth faculty has a low completion rate, it might indicate a need for better academic support.

## 🍳🥘🍲 Code 🍲🥘🍳
- Terlampir code sebagai berikut:
  
```
library(ggplot2)
#Menggunakan package openxlsx
library(openxlsx)

#Membaca file mahasiswa.xlsx
mahasiswa <- read.xlsx("https://storage.googleapis.com/dqlab-dataset/mahasiswa.xlsx",sheet = "Sheet 1")

#Menghitung Jumlah Data by Fakultas
summarybyfakultas <- aggregate(x=mahasiswa$JUMLAH, by=list(Kategori=mahasiswa$Fakultas, Tahun=mahasiswa$ANGKATAN), FUN=sum)
summarybyfakultas <- setNames(summarybyfakultas, c("fakultas","tahun", "jumlah_mahasiswa"))
summarybyfakultas

summarybyfakultas$tahun = as.factor(summarybyfakultas$tahun)

ggplot(summarybyfakultas, aes(x=fakultas, y=jumlah_mahasiswa)) + 
  geom_bar(stat = "identity", aes(fill = tahun), width=0.8, position = position_dodge(width=0.8)) + 
  theme_classic() 
```

## 🍳🥘🍲 Result 🍲🥘🍳

![image](https://github.com/diantyapitaloka/College-Trend/assets/147487436/43feb77c-c87c-4faf-8cfa-155559f666fd)

Dari grafik di atas terlihat peningkatan secara konsiten dari tahun ke tahun oleh fakultas "ICT" dan "Seni dan Desain". Di samping itu, Fakultas "D3 perhotelan" juga terlihat baru muncul di tahun 2017. Untuk fakultas "Bisnis" dan "Ilmu Komunikasi" terlihat fluktuasi jumlah mahasiswa selama tiga tahun.

## 🍳🥘🍲 Copyright 🍲🥘🍳
By Diantya Pitaloka
