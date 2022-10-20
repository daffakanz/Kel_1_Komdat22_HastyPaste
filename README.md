# Komdatcoba
Repository tugas UTS komdat 2022

<p style="font-size:100px"><b>Hasty Paste</b></p>

# Sekilas Tentang "Hasty Paste
<p>Deskripsi Judul. [Isi disini]</p>

# Instalasi
<p style="font-size:14px"><b>Prasyarat Sebelum instalasi</b></p>
<ol>
<li>Docker</li>
</ol>
<b>Langkah instalasi dalam CLI dengan docker</b>
<ol>
<li>

Langkah-langkah yang diperlukan adalah sebagai berikut : 

<b>Docker</b>

Update APT
  ```
  sudo apt update
  sudo apt install -y docker.io
  ```
Buka file policy-rc.d
  ```
  nano /usr/sbin/policy-rc.d
  ```
Lalu ubah 101 menjadi 0

Kemudian install requirements lainnya
  ```
  sudo apt-get install ca-certificates curl gnupg lsb-release
  ```
Keyrings
  ```
  sudo mkdir -p etc/apt/keyrings
  
  curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
  
  echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
  ```
Plugins
  ```
  sudo apt-get update
  sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin
  ```
Cek Status docker
  ```
  service docker status
  ```
<b>Pemasangan Hasty Paste dengan docker</b>
  ```
  sudo apt install git
  ```
Buat file baru di folder tempat app ingin di install

  ```
  touch docker-compose.yml
  nano docker-compose.yml
  ```
  
Salin teks berikut pada docker-compose.yml
  ```
  version: "3"

  services:
    paste-bin:
      container_name: paste-bin
      image: ghcr.io/enchant97/hasty-paste:1
      restart: unless-stopped
      volumes:
      - data:/app/data
      ports:
      - 8000:8000
      environment:
      - "UI_DEFAULT__USE_LONG_ID=False"

  volumes:
    data:
  ```
Pastikan docker sudah berjalan (status)

Jalankan docker-compose
  ```
  docker compose up -d
  ```
Cek status deployment
  ```
  docker ps
  curl 0.0.0.0:8000
  ```
  
</li>
</ol>

# Maintenance
  Untuk melakukan penghapusan paste yang telah expired
    ```
    cli cleanup -y --expired
    ```
  Untuk melakukan penghapusan seluruh paste yang telah melebihi waktu 365 hari
    ```
    cli cleanup -y --older-than 365
    ```

  Atau menggabungkan penghapusan paste yang telah expired dan melebihi waktu 365 hari
    ```
    cli cleanup -y --expired --older-than 365
    ```


# Cara Pemakaian
<ul>
<li><p>Tampilan aplikasi web</p></li>
<b>Tampilan pada desktop</b>
  <p><center><img src="images/tampilandesktop.png" width="500" ></center></p>

  <p><b>Fungsi utama</b></p>
    <li>Untuk memulai menulis note, tekan tombol "New Paste"</li>
    <li>Kemudian masukan "Title" "Waktu expiry note", "Syntax Highlight" tidak harus diisi</li>
    <center><img src="images/func1.png" width="500" ></center>

  Hasilnya akan seperti ini:
    <center><img src="images/func2.png" width="500" ></center>
    <li>Selanjutnya anda dapat mengunduh note tersebut dengan menekan tombol "Download"</li>
    <li>Anda dapat menekan tombol "Copy Share Link" untuk membagikan note tersebut</li>
    <li>Apabila anda ingin menduplikat dan mengedit notenya dapat menekan tombol "Clone & Edit"</li>


  
# Pembahasan
<p>kesimpulan fungsi "Judul" atau pendapat[isi disini].</p>

<p style="font-size:14px"> - Kelebihan Hasty Paste :</p>
<ul>
<li>Tidak memerlukan database.</li>
<li>Memakai jumlah resources yang kecil.</li>
<li>Tidak memerlukan Auth dan Javascript</li>
</ul>

<p style="font-size:14px"> - Kekurangan Hasty Paste :</p>
<ul>
<li>tralala4</li>
</ul>
  
<p style="font-size:14px"> - Bandingkan dengan aplikasi weblain yang sejenis :</p>
<ul>
<li>tralala5</li>
</ul>

# Referensi
<ul>
<li>link tralala</li>
</ul>
