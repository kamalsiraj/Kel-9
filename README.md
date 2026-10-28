nama = input("Masukkan nama Anda: ")
berat = float(input("Masukkan berat badan Anda (dalam kg): "))
tinggi = float(input("Masukkan tinggi badan Anda (dalam meter): "))
tidur = int(input("Masukkan jumlah jam tidur Anda per hari: "))
langkah = int(input("Masukkan jumlah langkah yang Anda lakukan per hari: "))

bmi = berat / (tinggi ** 2)

if bmi < 18.5:
    kategori_bmi = "Di Bawah Rentang Normal"
elif 18.5 <= bmi < 25:
    kategori_bmi = "Rentang Umum"
elif 25 <= bmi < 30:
    kategori_bmi = "Di Atas Rentang Normal"
else:
    kategori_bmi = "Obesitas"

if tidur < 7:
    kategori_tidur = "Perhatikan Durasi Tidur Anda"
else:
    kategori_tidur = "Durasi Tidur Anda Cukup"

if langkah < 8000:
    kategori_langkah = "Target Langkah Harian Anda Belum Tercapai"
else:
    kategori_langkah = "Target Langkah Harian Anda Telah Tercapai"

print("\nHasil Analisis Kesehatan untuk", nama)
print("BMI Anda:", round(bmi, 2), "-", kategori_bmi)
print("Jumlah Jam Tidur:", tidur, "-", kategori_tidur)
print("Jumlah Langkah:", langkah, "-", kategori_langkah)
