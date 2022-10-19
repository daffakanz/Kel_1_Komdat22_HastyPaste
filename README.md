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
<li>Get the code:

~~~
git clone https://github.com/fsinfuhh/Bitpoll
~~~

Generate a Python virtualenv and install dependencies:

```
virtualenv -p $(which python3) .pyenv
source .pyenv/bin/activate
pip install -r requirements.txt
```

Copy `bitpoll/settings_local.sample.py` to `bitpoll/settings_local.py` and customize the local settings.
  
Install Dependencies for Production:

```bash
sudo apt install g++ make python3-psycopg2 python3-ldap3 gettext gcc python3-dev libldap2-dev libsasl2-dev
```

Install Python Dependencies

```
pip install -r requirements-production.txt
```

Configure examples are in `settings_local.py`

our used uwsgi config can be found at
<https://github.com/fsinfuhh/mafiasi-rkt/blob/master/bitpoll/uwsgi-bitpoll.ini>

For Production systems it is nessesarry to run

```bash
./manage.py compilemessages
./manage.py collectstatic
```

# Management of Dependencies

We use pip-tools to manage the dependencies.
After modification or the requirements*.in files or for updates of packages run

```bash
pip-compile --upgrade --output-file requirements.txt requirements.in
pip-compile --upgrade --output-file requirements-production.txt  requirements-production.in requirements.in
```

to sync your enviroment with the requirements.txt just run

```bash
pip-sync
```

this will install/deinstall dependencies so that the virtualenv is matching the requirements file
  
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
