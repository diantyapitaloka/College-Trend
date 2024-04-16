## 🍳🥘🍲 College-Trend 🍲🥘🍳
Trend Jumlah Mahasiswa dari Tahun ke Tahun
- Grafik batang yang telah ditampilkan sebelumnya cukup baik. Namun, informasi yang terkandung masih belum diekplorasi lebih detail. Sebagai contoh, bagaimanakah jika kita ingin melihat trend jumlah mahasiswa tiap fakultas dari tahun ke tahun?

## 🍳🥘🍲 Code 🍲🥘🍳
'''
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
'''

## 🍳🥘🍲 Result 🍲🥘🍳

![image](https://github.com/diantyapitaloka/College-Trend/assets/147487436/43feb77c-c87c-4faf-8cfa-155559f666fd)

Dari grafik di atas terlihat peningkatan secara konsiten dari tahun ke tahun oleh fakultas "ICT" dan "Seni dan Desain". Di samping itu, Fakultas "D3 perhotelan" juga terlihat baru muncul di tahun 2017. Untuk fakultas "Bisnis" dan "Ilmu Komunikasi" terlihat fluktuasi jumlah mahasiswa selama tiga tahun.

## 🍳🥘🍲 Copyright 🍲🥘🍳
By Diantya Pitaloka
