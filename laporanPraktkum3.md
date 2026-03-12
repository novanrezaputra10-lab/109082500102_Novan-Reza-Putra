### 3. PT POS membutuhkan aplikasi perhitungan biaya kirim berdasarkan berat parsel. Maka, buatlah program BiayaPos untuk menghitung biaya pengiriman tersebut dengan ketentuan sebagai berikut! Dari berat parsel (dalam gram), harus dihitung total berat dalam kg dan sisanya (dalam gram). Biaya jasa pengiriman adalah Rp. 10.000,- per kg. Jika sisa berat tidak kurang dari 500 gram, maka tambahan biaya kirim hanya Rp. 5,- per gram saja. Tetapi jika kurang dari 500 gram, maka tambahan biaya akan dibebankan sebesar Rp. 15,- per gram. Sisa berat (yang kurang dari 1kg) digratiskan biayanya apabila total berat ternyata lebih dari 10kg.

```go
package main

import "fmt"

func main() {
	var bp, sb, d1, bk, bj, tb int

	fmt.Print("Berat Parsel (gram): ")
	fmt.Scan(&bp)

	d1 = bp / 1000
	sb = bp % 1000

	if sb >= 500 && bp <= 10000 {
		bk = sb * 5
	} else if sb < 500 && bp <= 10000 {
		bk = sb * 15
	} else {
		bk = sb * 0
	}

	bj = d1 * 10000
	tb = bj + bk

	fmt.Printf("Detail berat: %d kg + %d gr\n", d1, sb)
	fmt.Printf("Detail biaya: Rp. %d + Rp. %d\n", bj, bk)
	fmt.Printf("Total biaya pengiriman: Rp. %d\n", tb)
}
	
```
### Output Unguided :

##### Output 
![Screenshot Output Unguided C](https://github.com/novanrezaputra10-lab/109082500102_Novan-Reza-Putra/blob/main/modul2/output/soalC.png)
Ketika program dijalankan, kita diminta untuk memasukkan berat parsel dalam satuan gram. Setelah itu, program akan menghitung sisa berat dari parsel tersebut terlebih dahulu. Kemudian program akan mengecek kondisi sisa beratnya. Jika sisa beratnya tidak kurang dari 500 gram, maka akan dikenakan biaya tambahan sebesar Rp5 per gram. Jika sisa beratnya kurang dari 500 gram, maka biaya tambahannya sebesar Rp15 per gram. Namun, jika berat parsel lebih dari 10 kg, maka tidak akan dikenakan biaya tambahan. Setelah semua perhitungan selesai, program akan menampilkan hasil dari perhitungan tersebut sebagai output.