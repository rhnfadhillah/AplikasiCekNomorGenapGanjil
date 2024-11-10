
# Aplikasi Cek Nomor Ganjil / Genap    
Tugas 1 - Muhammad Raihan Fadhillah 2210010404
## Deskripsi
Aplikasi Cek Nomor adalah sebuah aplikasi sederhana berbasis Java yang digunakan untuk mengecek apakah sebuah angka yang dimasukkan oleh pengguna adalah bilangan genap, bilangan ganjil, dan juga apakah angka tersebut merupakan bilangan prima.

## Daftar Isi
- [Deskripsi](#deskripsi)
- [Prerequisites](#prerequisites)
- [Fitur](#fitur)
- [Cara Menjalankan](#cara-menjalankan)
- [Dokumentasi](#dokumentasi)
- [Screenshots](#screenshots)
- [Contoh Penggunaan](#contoh-penggunaan)
- [Pembuat](#pembuat)

## Prerequisites
Sebelum menjalankan aplikasi ini, pastikan Anda telah menginstal:
- Java Development Kit (JDK) versi 8 atau yang lebih baru.
- IDE seperti IntelliJ IDEA, Eclipse, atau NetBeans untuk menjalankan dan mengembangkan aplikasi.

## Fitur   
1. Memasukkan angka dan mengecek apakah angka tersebut genap atau ganjil.

2. Memeriksa apakah angka tersebut merupakan bilangan prima.

3. Menampilkan hasil pemeriksaan dalam bentuk dialog.

## Cara Menjalankan
1. Clone atau Download Repository:
    - Clone repository ini atau download sebagai ZIP dan ekstrak.

2. Buka Proyek di IDE:
    - Buka IDE Anda dan import proyek Java yang telah diunduh.

3. Jalankan Aplikasi:
    - Jalankan kelas AplikasiCekNomor dari IDE Anda.

4. Masukkan Angka:
    - Ketikkan angka pada kolom yang disediakan dan klik tombol "CEK!" untuk melihat hasilnya.
  
## Dokumentasi
Method Utama
- Method untuk cek bilangan prima
``` java
 private boolean apakahPrima(int n) {
    if (n <= 1) return false;
    for (int i = 2; i * i <= n; i++) {
        if (n % i == 0) return false;
    }
    return true;
```

- Method untuk cek bilangan ganjil atau genap
```java
 private void cek_btnActionPerformed(java.awt.event.ActionEvent evt) {                                        
        // TODO add your handling code here:
        int angka = Integer.parseInt(a1_field.getText());
        String hasil = "";
        if (!(angka == 0 || angka < 1)) {
            if (angka % 2 == 0) {
                hasil = "Bilangan Genap";
            } else if (angka % 2 == 1) {
                hasil = "Bilangan Ganjil";
            }

            if (apakahPrima(angka)) {
                hasil += " dan Prima";
            } else {
                hasil += " dan Bukan Prima";
            }

            JOptionPane.showMessageDialog(this, "Hasil : " + hasil);
            }
        else {
            JOptionPane.showMessageDialog(rootPane, "Masukkan Angka yang Valid", "Error", JOptionPane.ERROR_MESSAGE);
        }
        
    }                  
```
- Method untuk menghandle inputan hanya angka
``` java
private void a1_fieldKeyTyped(java.awt.event.KeyEvent evt) {                                  
        // TODO add your handling code here:
        char input = evt.getKeyChar();
        if (!Character.isDigit(input)) {
            evt.consume();  // Mencegah input selain angka
        }
    }        
```
- Method focus gained
``` java
private void a1_fieldFocusGained(java.awt.event.FocusEvent evt) {                                     
        // TODO add your handling code here:
        a1_field.setText("");
    } 
```

## Screenshots
![Screenshot 2024-11-10 164558](https://github.com/user-attachments/assets/edd145e4-f7e7-43f3-8159-261f63839678)



## Contoh Penggunaan

1. **Memasukkan Angka**:

   - Pengguna memasukkan angka ke dalam field input.
2. **Menekan Tombol Cek**:

   - Setelah memasukkan angka, pengguna menekan tombol "CEK!".

3. **Menampilkan Hasil**: 
   - Aplikasi akan menampilkan hasil dalam bentuk dialog yang menunjukkan sifat angka yang dimasukkan.


## Pembuat

- Nama : Muhammad Raihan Fadhillah
- NPM : 2210010404

