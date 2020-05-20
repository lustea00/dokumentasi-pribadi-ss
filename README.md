# Saya Tidak Tahu Ini Harus Dikasih Judul Apa


## Beberapa Tip Untuk Anda Yang Bekerja Di Backend
### Persiapan project
- Copy folder extensi yang ada di C:/sharedfolder/didin ke folder_project_anda/app/src
- Copy folder js yang ada di C:/sharedfolder/didin ke folder_project_anda/app
- Copy folder css yang ada di C:/sharedfolder/didin ke folder_project_anda/app
- Instal silvertripe softdeletable pakai composer
- Buka File folder_project_anda/app/_config/mysite.yml lalu tambahkan text ini
  ![N|Solid](./gambar/gambar-0.PNG)
  ![N|Solid](./gambar/gambar-1.PNG)
  ![N|Solid](./gambar/gambar-2.PNG)

### Tambah dan Hilangkan Filter
- Buka folder_project_anda/app/src/extensi/FilterExtension.php
- Ubah fungsi ini jika anda ingin menghilangkan beberapa filter. Isi key dengan nama DataObject anda dan value dengan nama field yang akan dihilangkan
  ![N|Solid](./gambar/gambar-3.PNG)
- Ubah fungsi ini jika anda ingin menambahkan beberapa filter. Isi key dengan nama DataObject anda dan value dengan field yang akan diisi (note: pastikan nama fieldnya unik)
  ![N|Solid](./gambar/gambar-4.PNG)

###  Required Form
- Buka folder_project_anda/app/js/Validation.js
- Untuk form utama ubah varibel ini. Isi key dengan nama DataObject anda dan value dengan nama field yang required
  ![N|Solid](./gambar/gambar-5.PNG)
- Untuk detail ubah variabel ini. Isi key dengan nama DataObject anda dan value dengan nama grid field yang juga punya value array
  ![N|Solid](./gambar/gambar-6.PNG)

### Beberapa Custom Form yang disesuaikan dengan standar MGE
- AutoNumericField. Tersedia dalam beberapa class ('two-comma', 'two-comma-min', 'without-comma', 'without-comma-min')
  ![N|Solid](./gambar/gambar-7.PNG)
- TanggalField
  ![N|Solid](./gambar/gambar-8.PNG)

## EphiliaTable
- Buat class baru yang extends EphiliaTable
#### Buat variabel dan fungsi berikut:
- `public static $title = "...";` untuk setting title
- `public static $tableName = "...";` untuk setting nama tabel
- `public static $canCreate = true/false;` untuk setting bisa buat data baru atau tidak
- `public static $canDelete = true/false;` untuk setting bisa hapus data atau tidak
- `public static $canEdit = true/false;` untuk setting bisa edit data atau tidak
- `public static $tableData = ['Nama Kolom/fungsi' => 'Label'];` untuk setting bisa hapus data atau tidak
- `public static $filterAction = ['Nama Field' => 'LIKE/='];` untuk setting filter
- `public function validationFields() {return ['NamaField' => ['required/max/min/dll' => 'value yang akan divalidasi']];}` untuk validasi field
- `public function getList($param){return DataObject::get();}` untuk setting list mana yang akan ditampilkan





