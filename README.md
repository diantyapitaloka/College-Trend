## 🍳🥘🍲 College-Trend 🍲🥘🍳
- The bar chart displayed previously is quite good. However, the information it contains has not yet been explored in detail. For example, what if we want to see the trend in the number of students for each faculty from year to year
- Comparing the percentage of students in each faculty helps identify which departments are expanding the fastest. This allows the university to allocate resources and staff more effectively based on demand.
- Analyzing the ratio of male to female students within specific faculties can highlight progress in diversity and inclusion. These insights are essential for creating targeted recruitment strategies for underrepresented groups.

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
