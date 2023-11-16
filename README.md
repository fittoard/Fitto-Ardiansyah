# UTS-METODE-NUMERIK
UTS METODE NUMERIk
1.	Persamaan non linier yang diberikan adalah:

3 + x^3 - x = 4

Mari kita cari solusi dari persamaan non-linier 3+x3−x=4. Persamaan ini dapat direduksi menjadi x3−x−1=0.
Saya akan menggunakan metode Newton-Raphson untuk mencari solusinya. Sebelumnya, kita perlu mendefinisikan fungsi dan turunan pertama dari fungsi tersebut.
Fungsi Persamaan: f'(x)=x3−x−1
Turunan Pertama:  f′(x)=3x2−1
Selanjutnya, kita dapat menggunakan metode Newton-Raphson dengan tebakan awal x0=1.0 dan toleransi 1×10−6. atau jawabannya ialah
Solusi akhir: x = 1.3247179572447898

Program untuk solusi diatas:


\python\


def fungsi(x):
    return x**3 - x - 1

def turunan_fungsi(x):
    return 3*x**2 - 1

def metode_newton_raphson(tebakan_awal, toleransi, max_iter):
    x = tebakan_awal
    for i in range(max_iter):
        x_baru = x - fungsi(x) / turunan_fungsi(x)
        if abs(x_baru - x) < toleransi:
            return x_baru
        x = x_baru
    return None

# Menentukan tebakan awal, toleransi, dan jumlah iterasi maksimum
tebakan_awal = 1.0
toleransi = 1e-6
max_iter = 100

# Memanggil fungsi metode_newton_raphson
solusi = metode_newton_raphson(tebakan_awal, toleransi, max_iter)

# Menampilkan solusi akhir
if solusi is not None:
    print(f"Solusi akhir: x = {solusi}")
else:
    print("Metode Newton-Raphson tidak konvergen.")

\python\

Output program diatas : x = 1.3247179572447898






2.Persamaan linier yang diberikan adalah:
     2x - 4 = 8
     Untuk menemukan nilai \(x\) yang memenuhi persamaan ini, kita dapat menyusun langkah-langkah sebagai berikut:

1. **Isolasi x:
   2x - 4 = 8dapat dipecahkan dengan menambahkan 4 ke kedua sisi persamaan:
   2x = 12

2. **Pembagian oleh Koefisien (x):
   Bagi kedua sisi persamaan dengan koefisien 2:
   x = 6

Jadi, solusi dari persamaan linier 2x - 4 = 8 adalah x = 6.


Program untuk solusi diatas :

\python\


def cari_solusi_persamaan_linier(a, b):
    # Isolasi x: ax + b = 0
    x = -b / a
    return x

# Menentukan koefisien a dan b dari persamaan 2x - 4 = 8
a = 2
b = -4 - 8

# Memanggil fungsi untuk mencari solusi
solusi = cari_solusi_persamaan_linier(a, b)

# Menampilkan solusi
print(f"Solusi dari persamaan {a}x + ({b}) = 0 adalah x = {solusi}")

\python\

Output program diatas :Solusi dari persamaan 2x + (-12) = 0 adalah x = 6






