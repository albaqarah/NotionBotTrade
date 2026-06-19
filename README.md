# NotionBotTrade
Test
Belum termasuk API key asli—**sengaja tidak aku masukkan** demi keamanan.

Di ZIP itu sudah ada file:

```
.env.example
```

Nanti setelah kamu `git clone` di VPS, kamu lakukan:

```bash
cp .env.example .env
nano .env
```

Lalu isi API Binance kamu di file `.env`:

```
BINANCE_API_KEY=isi_api_key_kamu
BINANCE_API_SECRET=isi_api_secret_kamu
```

File `.env` sudah masuk `.gitignore`, jadi **tidak akan ikut ke-upload ke GitHub** kalau kamu commit/push project-nya. Yang di-upload hanya `.env.example` sebagai template.

Alur amannya:

```bash
git clone https://github.com/username/nama-repo.git
cd nama-repo
cp .env.example .env
nano .env
pip install -r requirements.txt
python -m bot
```

Catatan penting: saat masih testing, biarkan ini:

```
DRY_RUN=true
USE_TESTNET=true
```

Artinya bot **belum kirim order live**. Kalau nanti sudah siap live, baru ubah:

```
DRY_RUN=false
USE_TESTNET=false
```
