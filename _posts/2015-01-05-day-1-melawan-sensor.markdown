---
author: firdausmubarik
comments: true
date: 2015-01-05 06:53:52+00:00
layout: post
link: http://firdausmubarik.com/2015/01/day-1-melawan-sensor/
slug: day-1-melawan-sensor
title: 'Day 1: Melawan Sensor'
wordpress_id: 85
categories:
- Digital Life
tags:
- IT
- Security
---

Sudah berkali-kali saya mendengar orang mengeluh berbagai situs kena sensor regim Kementerian Komunikasi dan Informasi (Kominfo) yang dimulai jaman menkominfo paling kontoversial: Pak Tif. Proyek yang dikenal dengan Internet Sehat, [Nawala](https://twitter.com/dns_nawala) punya dua kekurangan:

**Pertama**, gak cuma konten yang dianggap bermasalah situs sharing video seperti Vimeo juga kena. Saya juga sering melihat berbagai [situs berita](https://lh6.googleusercontent.com/-W9ZmZ9XhevE/VIR1GBMSjaI/AAAAAAAALEg/hbpl6SzwCFk/w428-h761-no/Screenshot_2014-12-07-21-45-33.png) yang kena sensor entah seluruh artikel atau bagian tertentu (slideshow misalnya).

**Kedua**, awalnya proyek Nawala yang berbasis DNS adalah pilihan. Pengguna yang tidak suka dengan Nawala bisa akses situs-situs yang diblok dengan ganti DNS seperti milik google di 8.8.8.8. dan 8.8.4.4. Namun kini semua DNS yang tidak berafiliasi dengan Nawala difilter dari ISP. Kasus ini sudah saya cek pada operator BizNet dan Telkom Speedy.

**Bagaimana bypass sensor DNS?**

**Windows** dan **OSX** gunakan [**DNSCrypt**](http://dnscrypt.org/) yang didukung [OpenDNS](https://www.opendns.com/about/innovations/dnscrypt/). Pada dasarnya DNSCrypt bekerja di background dan berjalan sebagai service. Bahan dasar DNSCrypt bisa di download di: http://download.dnscrypt.org/dnscrypt-proxy/

Supaya mudah install juga versi GUI untuk konfigurasi.

**Windows**

Bahan



	
  1. [http://download.dnscrypt.org/dnscrypt-proxy/dnscrypt-proxy-win32-full-1.4.1.zip](http://download.dnscrypt.org/dnscrypt-proxy/dnscrypt-proxy-win32-full-1.4.1.zip) dari [http://download.dnscrypt.org/dnscrypt-proxy/](http://download.dnscrypt.org/dnscrypt-proxy/)

	
  2. [DNSCrypt Windows Service Manager 0.2](http://simonclausen.dk/dnscrypt-winservicemgr/DNSCrypt%20Windows%20Service%20Manager.zip)


Langkah

	
  1. Download dua aplikasi diatas dan extract di tempat yang sama. misal C:/dnscrypt

	
  2. click aplikasi dnscrypt-winservicemgr.exe

	
  3. pliih network adapter dan pencet "ENABLE".


Note: gamber menyusul, windows tidak tersedia di meja

**OSX**

Instalasi di OSX akan melalui homebrew sekaligus mempermudah hidup kita sebagai pengguna OSX ke depan. Langkah



	
  1. buka Terminal dan kopi paste:

    
    <code>ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"</code>




	
  2. lalu install DNSCrypt

    
    <code>brew install wget</code>




	
  3. Download [DNSCrypt Client](Download%20dnscrypt-osxclient-1.0.4.dmg) dari https://github.com/alterstep/dnscrypt-osxclient

	
  4. Jalankan aplikasi dari dmg (atau pindahkan ke Application)

	
  5. di tabbar akan muncul icon baru, nyalakan DNSCrypt


![](http://firdausmubarik.com/wp-content/uploads/2015/01/Screen-Shot-2015-01-05-at-1.37.19-PM.png)

![](http://firdausmubarik.com/wp-content/uploads/2015/01/Screen-Shot-2015-01-05-at-1.44.47-PM.png)

**Smartphone**

Saya belum menemukan implementasi DNSCrypt yang mudah, sementara gunakan Opera Mini, dengan sistem kompresi yang memutar jalur ke server Opera praktis Nawala DNS dibypass.

**Skala Network**

Bagaimana jika ingin implementasi ini dalam skala lebih besar misalkan di rumah, kantor atau cafe? saya rasa akan banyak kantor media yang terganggu dengan akses yang diblokir. Solusinya implementasi DNSCrypt di router. Bahan dasarnya sama tinggal memilih router + custom firmwware + DNSCrypt. Dengan implementasi di router, masing-masing device tidak perlu disetting khusus.



	
  * Tulisan ini adalah bagian dari tantangan menulis satu tahun FirdausMubarik.com


