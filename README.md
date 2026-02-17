## 🍳🥘🍲 College-Trend 🍲🥘🍳
- The bar chart displayed previously is quite good. However, the information it contains has not yet been explored in detail. For example, what if we want to see the trend in the number of students for each faculty from year to year.
- The "speed-to-lead" metric is more critical than ever. In 2026, leading institutions are moving beyond basics chatbots to Agentic AI systems. These assistants don't just answer FAQs; they help prospective students navigate complex financial aid forms, schedule tours, and even provide personalized program recommendations based on a student’s interests and past academic performance, significantly reducing "summer melt" (the drop-off between acceptance and enrollment).
- In an era of skepticism toward degree value, students are increasingly looking for a clear ROI. By integrating labor market data (e.g., Lightcast or LinkedIn insights), universities can map their current curriculum against real-time job demand. If a specific faculty shows high enrollment but low job-placement "fit" in the current economy, the university can proactively pivot to include stackable micro-credentials or industry-standard certifications within the traditional degree path.
- Modern enrollment isn't just about getting students in; it’s about ensuring they are healthy enough to stay. Data tracking has expanded to include non-academic indicators, such as participation in campus clubs, recreational facility usage, and visits to student health services. Identifying a sudden drop in a student’s social or physical engagement acts as a "soft" early warning for mental health burnout, allowing the university to offer support before it affects their grades.
- Gen Z and Gen Alpha are increasingly prioritizing a university's environmental footprint. Tracking a campus’s carbon neutrality progress, green building certifications, and "climate-forward" curriculum can actually be a recruitment lever. Data-driven reporting on the university’s sustainability goals helps marketing teams appeal to "eco-conscious" applicants who view the physical campus as a living laboratory for the future.
- While traditional enrollment data tracks diversity in numbers, 2026 strategies focus on persistence parity. By analyzing the retention rates of first-generation and underrepresented students at a granular, faculty-by-faculty level, universities can identify "inclusion gaps." If a specific department has high minority enrollment but low graduation rates, it signals a need for targeted mentorship programs or a more inclusive curriculum, rather than just more marketing.
- With the rise of the "swirling student" (those who attend multiple institutions), the ease of credit transfer is a major enrollment driver. Universities are now using data to identify exactly where prospective transfer students lose credit hours. By automating the "Credit for Prior Learning" (CPL) process and offering transparent, real-time transfer evaluations, a university can become the "institution of choice" for the growing population of community college graduates and returning adult learners.
- Campus "Micro-Climate" Enrollment Drivers: Sometimes, enrollment spikes aren't caused by the curriculum, but by specific "star" faculty or high-profile research labs. Identifying these "magnet" individuals or facilities helps the university understand which internal assets are the strongest drivers of its national ranking and applicant interest.
- Non-Traditional & Adult Learner Growth Trends: With the "demographic cliff" affecting high school graduate numbers, tracking the rise of adult learners (25+) is vital. Data on part-time vs. full-time status within this group helps the university decide if it needs to expand evening childcare, flexible bursaries, or professional "micro-credentials" alongside traditional degrees.
- Competitor Benchmarking & Market Share Analysis: Enrollment doesn't happen in a vacuum. Analyzing "cross-admit" data—where students who were accepted to your university chose to go instead—reveals which rival institutions are winning over your target demographic. This identifies whether your loss is due to their better financial aid, specific facilities, or program prestige.
- Social Sentiment & Brand Perception Mapping: Tracking mentions of specific faculties or campus life on social media and student forums provides a "real-time" pulse of the university's reputation. If a faculty's enrollment drops despite high job placement, sentiment analysis might reveal issues with campus culture or perceived "difficulty" that marketing needs to address.
- Predictive Attrition Modeling (Early Warning Systems): By integrating behavioral data (such as LMS login frequency, library usage, and mid-term grades), the university can move from tracking leakage to predicting it. This allows for "intrusive advising"—reaching out to a student before they even realize they are at risk of dropping out.
- High School Feeder School Analysis: Granular data on which secondary schools produce the most successful students allows recruitment teams to foster deeper institutional relationships. By identifying "under-performing" regions where the university has a low presence, marketing teams can host targeted workshops or open houses. This strategic outreach ensures a steady pipeline of diverse and well-prepared applicants year after year.
- Campus Infrastructure and Space Utilization: Analyzing the density of students per faculty relative to the physical capacity of their respective buildings prevents "classroom crowding" before it happens. As certain departments grow, data-driven insights allow for the proactive scheduling of lab spaces and lecture halls across the campus. This ensures that the physical environment evolves at the same pace as the student body's interests.
- Impact of Digital and Hybrid Learning: Comparing the growth of fully online programs versus traditional on-campus degrees highlights shifting student preferences for flexibility. This data is crucial for deciding whether to invest in physical brick-and-mortar expansions or in high-tech digital infrastructure. Understanding these modalities helps the university remain competitive in an increasingly globalized and remote-friendly education market.
- Alumni Career Path Integration: Linking historical enrollment data with the career outcomes of graduates provides a powerful recruitment tool for prospective students. If a specific "hybrid" major shows a 95% employment rate within six months, the university can lean into that data for marketing. This creates a feedback loop where market demand directly informs the expansion of specific academic departments.
- Economic Cycle Sensitivity: Correlating enrollment trends with national economic indicators, such as unemployment rates or industry-specific growth, reveals how sensitive certain majors are to the "real world." For example, business enrollment might spike during a recession while creative arts remain steady. These insights allow the university to "recession-proof" its offerings by diversifying the types of programs it promotes during different economic climates.
- Financial Aid and Enrollment Synergy: Mapping the distribution of scholarships and grants against enrollment spikes helps determine the true ROI of financial incentives. It allows the university to see if an increase in a specific faculty's population is driven by academic reputation or by more aggressive financial aid packages. Understanding this balance is key to maintaining a sustainable budget while attracting top-tier talent.
- Retention and Attrition Correlation: Tracking the flow of students from freshman year to graduation within specific faculties reveals where students are most likely to drop out or switch majors. By identifying these "leakage points," departments can implement targeted academic support or mentorship programs to improve overall completion rates. This longitudinal view ensures that high enrollment numbers actually translate into successful alumni.
- Comparing the percentage of students in each faculty helps identify which departments are expanding the fastest. This allows the university to allocate resources and staff more effectively based on demand.
- Analyzing the ratio of male to female students within specific faculties can highlight progress in diversity and inclusion. These insights are essential for creating targeted recruitment strategies for underrepresented groups.
- Breaking down enrollment by the students' home regions can reveal the university's geographic reach and brand reputation. This data is invaluable for marketing teams looking to expand into new provinces or international markets.
- Faculty-to-Student Ratio Optimization: Monitoring the growth of student enrollment alongside the hiring of new professors ensures that the quality of education does not suffer during growth spurts. If a faculty experiences a 20% enrollment jump without a corresponding increase in staff, the university can predict and prevent burnout or a drop in student satisfaction. Maintaining this ratio is a vital component of keeping national accreditation and high rankings.
- As modern careers evolve, students are increasingly drawn to programs that cross traditional faculty boundaries. Visualizing the rise of these hybrid majors can help the university design more relevant, future-proof curricula.
- External factors, such as changes in government funding or accreditation standards, often influence enrollment spikes or drops. Mapping these external events against your trend lines can explain sudden shifts in the data.
- Tracking student cohorts over time shows the specific years where students are most likely to leave the university. Identifying these "leakage points" per faculty is the first step toward improving student persistence.
- Linking enrollment numbers with graduation data per faculty reveals which departments are most successful at retaining students. If a high-growth faculty has a low completion rate, it might indicate a need for better academic support.

## 🍳🥘🍲 Code 🍲🥘🍳
- TPlease find the code below :
  
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
