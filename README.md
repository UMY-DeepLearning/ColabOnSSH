## Menghubungkan Google Colab dengan server SSH UMY

### Kebutuhan

Beberapa hal yang perlu di pasang di komputer lokal

- Windows 10 1804+ 
- Visual Studio Code + Remote SSH Extension

### Cara terhubung SSH

Buka visual studio code, hubungkan dengan ssh hubungkan dengan host user@ipaddress

``` powershell
ssh user@ipaddress
```

kemudian isi dengan password yang sudah diberikan.

### Menjalankan Jupyter

buka terminal dengan menekan <kbd>ctrl + ~</kbd> atau menu <kbd>Terminal</kbd> > <kbd>New Terminal</kbd>

jalankan perintah berikut dalam terminal bash.

``` powershell
jupyter notebook \
  --NotebookApp.allow_origin='https://colab.research.google.com' \
  --port=8889 \
  --NotebookApp.port_retries=0
```

Akan muncul forward port, tidak perlu di buka.

salin hasil keluaran program yang berbentuk seperti berikut.

```
http://localhost:8889/?token=25befd54017c923ece48e7f0a236f53bb4c8ed2183ffcedb
```

### Menghubungkan colab ke SSH

pada tampilan google colab, tekan drop down pada pojok kanan atas, disamping ram dan disk

lalu pilih <kbd>Connect To Local Runtime</kbd>

Timpa (paste) url yang sudah disalin, kemudian hubungkan.

Selesai, anda bisa menggunakan Colab tanpa batas server.
