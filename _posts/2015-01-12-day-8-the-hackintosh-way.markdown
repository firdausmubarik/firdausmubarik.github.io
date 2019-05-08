---
author: firdausmubarik
comments: true
date: 2015-01-12 19:49:45+00:00
layout: post
link: http://firdausmubarik.com/2015/01/day-8-the-hackintosh-way/
slug: day-8-the-hackintosh-way
title: 'Day 8: The Hackintosh Way'
wordpress_id: 110
categories:
- Digital Life
---

Hackintosh adalah metode untuk menginstall sistem operasi OSX di hardware yang tidak berasal dari Apple. Ini bisa dilakukan karena mulai OS X (sepuluh) Apple menggunakan hardware dari Intel, sama persis dengan komputer PC i386, juga dikenal IBM compatible, atau versi AMD64. Dengan fakta ini komputer dengan prosesor Intel dan AMD dapat menggunakan OSX. Tentu dengan sedikit perubahan.

Ada beberapa metode, yang pertama adalah dengan menyiapkan hardware semirip mungkin dengan yang digunakan Apple. Ingat mereka menggunakan part yang umum hanya dengan desain yang mereka pesan sendiri. Kalau pakai part yang mirip dengan Apple praktis instalasi berjalan sangat mulus dengan sedikit perubaham saja. Ini disebut Vanila install, dimana perubahan hanya dilakukan pada proses boot.

Ketika hardware yang digunakan jauh dari part yang dipakai Apple maka semakin banyak modifikasi yang diterapkan. Memilih modifikasi, testing, gagal dan mengulang lagi bukan hal yang ingin dilakukan semua orang. Kali ini termasuk saya :) untuk itu ada Distro, OSX yang telah dimodifikasi dengan berbagai mod-mod itu. Salah satu yang terbaik adalah Hackintosh.Zone dulu dikenal dengan Distro Niresh.

Saya disini gak bakal jelasin panjang lebar cara instalasi, justru lebih bakal cerita soal aplikasi dan modifikasi pribadi yang saya anggap penting anda ketahui.

OS: Hackintosh.Zone Yosemite

Download versi USB via torrent di , lalu jika anda punya OSX sebelumnya pakai package installer atau Windows installer. Tentu siapkan USB Flashdisk 8GB atau lebih. Paling aman jika memakai motherboard dengan chipset intel, prosesor intel core (i3, i5, i7) dan Graphic Card NVIDIA GTX 2xx ke atas.

Detail instalasi silahkan dilihat di

Clover

Dalam kasus saya entah kenapa bootloader Clover tidak terinstall paska Hackintosh.Zone selesai, sehingga saya tergantung dengan USB sebagai bootloader. Jika terjadi install Clover dan Clover Configurator

SWitchResX

Satu masalah lagi dengan dua monitor yang persis sama, layar utama gagal menampilkan resolusi Full HD. Saya malas mencoba konfigurasi layar di bootloader atau install driver baru, saat ini lebih banyak rugi waktu. So gunakan saja SwitchResX untuk merubah ukuran layar on the fly.

MUST HAVE

MPlayerX / VLC

Admit it, Quick Time is suck as suck as Windows Media Player. Mereka gagal memainkan banyak video, nampaknya mereka hanya di desain untuk memainkan video dari sistem mereka sendiri. Tidak satupun dalam pengalaman saya berhasil memainkan file MKV dengan benar. MPlayerX punya tampilan yang simple, memainkan AVI, MP4, MKV, MOV, WMV dan bisa memainkan video dari torrent yang masih di download. VLC punya interface yang enggak cocok, lebih lambat dan gagal memainkan file torrent yang belum rampung. Namun beberapa file yang gagal atau aneh di MplayerX bisa berjalan di VLC, install sebagai backup.

Skype

At the first its like, why Skype if we have Whatssapp or Line or Hangout. Come on who need Skype other than Long Distance Relationship? tapi Skype bisa chat, voice dan video conference. Transfer file drag n drop. Share layer (saya enggak pernah pakai), punya sistem P2P dan enrkipsi lumayan untuk komunikasi normal. Saya enggak sarankan Skype untuk komunikasi yang butuh keamanan tinggi. Ia bisa dipakai di hampir semua desktop dan mobile bahkan beberapa hardware khusus. Jika jangkauan dan kepasitian nyambung, Skype paling oke.

Dropbox

Dropbox adalah holy grail untuk sinkronisasi file. Mendukung history, selected sync, web access, share mudah. Buat user yang tidak puss dengan selected sync bisa membuat soft link directory. Sayangnya dibanding Google Drive dan One Drive yang member 15Gb free, tawaran 5Gb dari Dropbox terlalu kecil. Maka says gunakan Dropbox untuk file paling seeing dipakai antar komputer seperti: aplikasi kecil yang sulit download lagi, document dan foot yang seeing dipakai, template. Untuk arsip file lama gunakan Google Drive dan One Drive.

Disk Inventory X /Grand Perspective

Saya orang VISUAL. cara paling cepat mengetahui file apa yang menghabiskan Hard disk adalah dengan peta visual file-file tersebut. Grand Perspective dan Disk Inventory X kedunya gratis untuk digunakan. Pilih salah satu. Disk Inventory X lebih menang dengan kemampuang sort dan filter yang baik.

The Unarchiver

OSX sudah menyediakan program membuka file zip. Tapi ketauhilah zip bukan satu-satunya format mengkompres file/directory yang ada. RAR, Bunzip? The Unarchiver membuka hampir semua file yang diberikan ke saya.

DNSCrypt

Di jaman internet begini masih menyerahkan pilihan web yang bisa dibuka dan tidak pada negara? Apalagi pada mekominfo? Gunakan DNSCrypt untuk bypass software firewall negara. Selengkapnya baca di:

Libre Office

Lets make it clear. Sometimes I got file on email that need to be opened. Libre Office adalah aplikasi office gratis (pengolah kata, pengolah table, dan presentasi) yang memadai. Saya enggak may computer dibebani dengan apliksi office 2011 atau iWork. Keep it simple dude

uTorrent

Gunakan torrent untuk download, apapun!

Clean My Mac

Sometimes your Mac is not the Mac you wanted, its messy and dirty. Bersihkan file-file lama, recycle bin, aplikasi enggak kepake. Free up your Natal list. Clean My Mac to rescue

Homebrew

Okay, ini tool terakhir. Mungkin beberapa orang menganggap enggak perlu ya. Tapi install lah Homebrew agar hidup makin mudah.

Web Development

Sublime Text

My Favorite text editor. Melahap file HTML, CSS, JS dengan baik. Visual thumbnail!, multi column and row. Membuka satu file sama di beberapa jendela (edit bagian atas dan bawah bersamaan). Jika feature enggak ada di Sublime Text mungkin hanya perlu install plugins saja

Git

Simpan code-code kerjaan dengan baik, gunakan Git sebagai penyimpan history dan berbagi development. Saya rasa ini perlu post tersendiri untuk dibagas

CodeKit

Ini program paling ajaib di web development. Menggabungkan Sassy -> CSS3 preposesor, on the fly injection ke browser. Ia melakukan apa yang gagal lakukan oleo Adobe Dreamweaver dan Frontpage dengan bail.

Google Chrome + tons

Ini masih browser favorite, dengan tons of plugins untuk berganti resolusi, cek kode web, dan banyak lagi. Sayangnya ia kini mulai lambat. Saya tengah merubah kebiasaan membuka via Safari.

Mozila Firefox + Firebug

Ingin tahu code apa dibalik sebuah gambar website? Meski Chrome dan Firefox sudah menyedian inspection, tidak ada yang mengalahkan Mozilla Firefox + Firebug. Its the best!

Filezila

FTP thing, transfer file dari ke server. Gunakan Filezilla

Terminal

Ini tentu tersedia di semua OSX, hanya orang dungu enggak pakai terminal

Sketch 3

Program baru untuk prototyping dan membuat wireframe design.

Others

nvAlt

Untuk mengumpulkan catataan yang tersebar berantakan. Ini semacam buku saku kecil tempat mencatat ide.

Flux

Dulu saya enggak percaya kata ibu saya lampu bohlam kuning itu lebih enak buat tidur daripada lampu neon yang "putih" kini saya tahu bahwa cahaya warga biru (siang) membuat otak enggak ngantuk, sementara cahaya lebih kuning atau merah itu lebih santai di mata. Jika sering pakai komputer saat siang berganti malam. Gunakan mata orang lain!

Picasa

Untuk mengumpulan dan mengedit foto-foto secara cepat.

note: its so damn tired to write. I will stop here and continue tommorow
