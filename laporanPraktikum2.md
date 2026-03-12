### 2. Siswa kelas IPA di salah satu sekolah menengah atas di Indonesia sedang mengadakan praktikum kimia. Di setiap percobaan akan menggunakan 4 tabung reaksi, yang mana susunan warna cairan di setiap tabung akan menentukan hasil percobaan. Siswa diminta untuk mencatat hasil percobaan tersebut. Percobaan dikatakan berhasil apabila susunan warna zat cair pada gelas 1 hingga gelas 4 secara berturutan adalah ‘merah’, ‘kuning’, ‘hijau’, dan ‘ungu’ selama 5 kali percobaan berulang. Buatlah sebuah program yang menerima input berupa warna dari ke 4 gelas reaksi sebanyak 5 kali percobaan. Kemudian program akan menampilkan true apabila urutan warna sesuai dengan informasi yang diberikan pada paragraf sebelumnya, dan false untuk urutan warna lainnya.

```go

package main

import "fmt"

func main() {
	var i, j int
	var w1, w2, w3, w4 string
	var berhasil bool

	for i = 1; i <= 5; i++ {
		fmt.Print("Percobaan ", i, ": ")
		fmt.Scan(&w1, &w2, &w3, &w4)

		if w1 == "merah" && w2 == "kuning" && w3 == "hijau" && w4 == "ungu" {
			j++
		}

	}

	berhasil = j == 5
	fmt.Println("BERHASIL:", berhasil)
}
```
### Output Unguided :

##### Output 
![Screenshot Output Unguided 1_1](https://github.com/novanrezaputra10-lab/109082500102_Novan-Reza-Putra/blob/main/modul2/output/soalB.png)
Ketika program dijalankan, kita diminta untuk memasukkan empat urutan warna yaitu merah, kuning, hijau, dan ungu sebanyak lima kali percobaan. Setelah itu program akan memeriksa apakah setiap percobaan yang dimasukkan sudah sesuai dengan urutan warna yang benar atau belum. Percobaan dianggap berhasil jika urutan warna yang dimasukkan sama dengan urutan yang diminta. Setelah semua percobaan selesai, program akan menampilkan hasil dari variabel berhasil dalam bentuk nilai boolean yaitu true atau false.