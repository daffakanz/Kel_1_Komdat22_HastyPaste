# Komdatcoba
Repository tugas UTS komdat 2022

<p style="font-size:20px"><b>Coba "Bitpoll"</b></p>

<p style="font-size:14px">Sekilas Tentang "Bitpoll"</p>
<p>Deskripsi Judul.</p>
Bitpoll merupakan sebuah aplikasi berbentuk WebApps untuk dapat membuat sebuah jadwal rapat dan melakukan polling

<p style="font-size:20px"><b>Instalasi</b></p>
<p style="font-size:14px"><b>Prasyarat Sebelum instalasi</b></p>
<ol>
<li>tralala</li>
</ol>
<b>Langkah instalasi dalam CLI</b>
<ol>
<li>Ambil kode yang terdapat pada github berikut:

~~~
git clone https://github.com/fsinfuhh/Bitpoll
~~~

Buatlah Python virtualenv dan lakukan installasi dependencies:

```
virtualenv -p $(which python3) .pyenv
source .pyenv/bin/activate
pip install -r requirements.txt
```

Copy dan paste file `bitpoll/settings_local.sample.py` to `bitpoll/settings_local.py` untuk mengkustomisasi settingan lokal.
  
Installasi dependencies untuk produksi:

```bash
sudo apt install g++ make python3-psycopg2 python3-ldap3 gettext gcc python3-dev libldap2-dev libsasl2-dev
```

Installasi Python Dependencies

```
pip install -r requirements-production.txt
```

Configure examples are in `settings_local.py`

our used uwsgi config can be found at
<https://github.com/fsinfuhh/mafiasi-rkt/blob/master/bitpoll/uwsgi-bitpoll.ini>

Untuk Production systems, hal ini perlu dijalankan :

```bash
./manage.py compilemessages
./manage.py collectstatic
```

# Management of Dependencies

Untuk melakukan management pada dependencies
kita menggunakan library pip-tools dan melakukan modifikasi pada requirements*.in files atau untuk memperbarui packages run

```bash
pip-compile --upgrade --output-file requirements.txt requirements.in
pip-compile --upgrade --output-file requirements-production.txt  requirements-production.in requirements.in
```
Untuk melakukan sinkronisasi environment dengan requirement.txt dapat dijalankan

```bash
pip-sync
```
Hal ini akan melakukan installasi dan deinstallasi dependencies agar virtualenv dapat mencocokan file yang dibutuhkan

# Inisialisasi 
Initialise Database:

```
./manage.py migrate
```

Run Testserver:

```
./manage.py runserver
```
</li>
</ol>

<b>Cara Pemakaian</b>
<ul>
<li><p>Tampilan aplikasi web</p></li>

<li><p><b>Fungsi-fungsi utama</b></p></li>
</ul>

<b>Pembahasan</b>
<p>kesimpulan fungsi "Judul".<p>

Kelebihan Judul :
<ul>
<li>tralala3</li>
</ul>

Kekurangan Judul :
<ul>
<li>tralala4</li>
</ul>

<b>Referensi</b>
<ul>
<li>link tralala</li>
</ul>
