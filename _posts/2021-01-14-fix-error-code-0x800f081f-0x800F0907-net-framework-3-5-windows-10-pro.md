---
title: "Fix Error code: 0x800f081f / 0x800F0907 .NET Framework 3.5 Windows 10 Pro"
date: 2021-01-14
category: [ Software ]
tags: [ system ]
image: https://1.bp.blogspot.com/-rkXz6dd-Rf8/YABi7xT4ZZI/AAAAAAAADzU/9Rfm52_cZcoLPK2fzKpGZ1iet_oDdsPeACLcBGAsYHQ/s0/Fix%2BError%2Bcode%2B0x800f081f%2Bor%2B0x800F0907%2B.NET%2BFramework%2B3.5.jpg
---
Berikut ini pengalaman singkat saya ketika install Windows 10 Pro 64bit, kemudian saya lanjutkan <i>Change product key</i> (online activation) dan install drivers. Setelah kembali dari restart install drivers, terdapat notifikasi "<i>Error code: 0x800F0907 Microsoft .NET Framework 3.5</i>". Kemudian saya searching bagaimana cara fix error tersebut. Tetapi muncul error kode baru "<i>Error code: 0x800f081f</i>" yang ternyata mengharuskan saya untuk menggunakan USB flashdrive/bootable windows 10 yang baru saja saya gunakan untuk intall notebook (bisa juga menggunakan dvd).<br />
<br />
Caranya hubungkan USB flashdrive/bootable windows 10, cari aplikasi di Start menu "<i>Command Prompt</i>" kemudian klik kanan dan pilih "<i>Run as adminitrator</i>". Selanjutnya masuk kode di bawah ini dan tekan <i>Enter</i>:<br />
<br />
<i>dism /online /enable-feature /featurename:NetFX3 /Source:<b>[DRIVE]</b>:\sources\sxs /LimitAccess</i><br />
<br />
Untuk <b>[DRIVE]</b> silahkan ganti nama sesuai dengan inisial drive yang tertera, misalnya USB bootable windows 10 saya berada di (<b>D:</b>) maka hasilnya seperti pada contoh dibawah ini:<br />
<br />
<i>dism /online /enable-feature /featurename:NetFX3 /Source:<b>D:</b>\sources\sxs /LimitAccess</i><br />
<br />
Selanjutnya hanya tunggu hingga proses selesai.<br />
<br />
<i>*. Catatan</i>:<br />
Cara yang saya tulis ini mestinya harus sudah melewati proses tekan tombol <i>Windows-Key</i>+<i>R</i> kemudian ketik <i>gpedit.msc</i> pada "<i>Administrative Templates</i> > <i>System > Specify settings for optional component installaltion and component repair</i>" sudah di <i>Enable</i> dengan cara klik kanan > <i>Edit</i>.
