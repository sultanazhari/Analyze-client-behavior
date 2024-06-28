# Deskripsi Proyek
Kamu bekerja sebagai seorang analis di perusahaan operator telekomunikasi bernama Megaline. Perusahaan tersebut menawarkan kliennya dua jenis paket prabayar, yaitu paket Surf dan paket Ultimate. Departemen periklanan ingin mengetahui paket prabayar mana yang menghasilkan lebih banyak pendapatan sehingga mereka bisa membuat anggaran iklan yang sesuai. 

Oleh karena itu, kamu akan melakukan analisis awal untuk paket-paket prabayar tersebut berdasarkan sampel klien yang berukuran relatif kecil. Kamu memiliki 500 data klien Megaline yang berisi informasi seperti: siapa mereka, dari mana asalnya, jenis paket apa yang mereka gunakan, serta jumlah panggilan dan pesan yang mereka kirim di tahun 2018. Nah, tugasmu adalah menganalisis perilaku klien dan menentukan paket prabayar mana yang mendatangkan lebih banyak pendapatan. 

# Deskripsi paket prabayar
Catatan: Megaline membulatkan detik ke menit dan megabyte ke gigabyte. Untuk panggilan, setiap panggilan individual dibulatkan ke atas: bahkan jika suatu panggilan berlangsung hanya satu detik, panggilan tersebut akan dihitung sebagai satu menit. Untuk traffic web, setiap sesi web individual tidak dibulatkan ke atas. Akan tetapi, total untuk sebulan dibulatkan ke atas. Jika seorang pengguna menghabiskan 1025 megabyte bulan ini, dia pun akan dikenai biaya untuk 2 gigabyte.

- Surf

  - Biaya bulanan: $20
  - 500 menit durasi panggilan per bulan, 50 SMS, dan 15 GB data
  - Setelah melebihi batas paket, akan dikenakan:
  - 1 menit: 3 sen
  - 1 SMS: 3 sen
  - 1 GB data: $10

- Ultimate

  - Biaya bulanan: $70
  - 3000 menit durasi panggilan per bulan, 1000 SMS, dan 30 GB data
  - Setelah melebihi batas paket, akan dikenakan:
  - 1 menit: 1 sen
  - 1 SMS: 1 sen
  - 1 GB data: $7

# Deskripsi Data
Megaline membulatkan detik ke menit dan megabyte ke gigabyte. 
Untuk panggilan, setiap panggilan individual dibulatkan ke atas: bahkan jika suatu panggilan berlangsung hanya satu detik, panggilan tersebut akan dihitung sebagai satu menit. 
Untuk traffic web, setiap sesi web individual tidak dibulatkan ke atas. Akan tetapi, total untuk sebulan dibulatkan ke atas. 
Jika seorang pengguna menghabiskan 1025 megabyte bulan ini, dia pun akan dikenai biaya untuk 2 gigabyte.

Tabel users (data pengguna):

- user_id — ID pengguna
- first_name — nama depan pengguna
- last_name — nama belakang pengguna
- age — usia pengguna (tahun)
- reg_date — tanggal mulai berlangganan (dd, mm, yy)
- churn_date — tanggal pengguna berhenti menggunakan layanan (jika nilainya hilang atau tidak ada, berarti paket layanan sedang digunakan saat data ini dibuat)
- city — kota tempat tinggal pengguna
- plan — nama paket telepon
- Tabel calls (data panggilan):

  - id — ID panggilan unik
  - call_date — tanggal panggilan
  - duration — durasi panggilan (dalam menit)
  - user_id — ID pengguna yang melakukan panggilan
  
- Tabel messages (data SMS):

  - id — ID SMS unik
  - message_date — tanggal SMS dikirim
  - user_id — ID pengguna yang mengirim SMS
- Tabel internet (data sesi web):

  - id — ID sesi web unik
  - mb_used — volume data yang dihabiskan selama sesi (dalam megabyte)
  - session_date — tanggal sesi web
  - user_id — ID pengguna
- Tabel plans (data paket telepon):

  - plan_name — nama paket telepon
  - usd_monthly_fee — biaya bulanan dalam dolar AS
  - minutes_included — alokasi menit panggilan bulanan
  - messages_included — alokasi SMS bulanan
  - mb_per_month_included — alokasi volume data bulanan (dalam megabyte)
  - usd_per_minute — harga per menit jika sudah melebihi batas alokasi paket (misalnya, jika paket memiliki alokasi 100 menit maka penggunaan mulai dari menit ke-101 akan dikenakan biaya)
  - usd_per_message — harga per SMS jika sudah melebihi batas alokasi paket
  - usd_per_gb — harga per gigabyte tambahan data jika sudah melebihi batas alokasi paket (1 GB = 1024 megabyte)
