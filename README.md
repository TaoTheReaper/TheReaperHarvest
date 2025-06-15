# TheReaperHarvest

![Powered by TaoTheReaper](https://img.shields.io/badge/Powered%20by-TaoTheReaper-black?style=for-the-badge&logo=skynet)

**TheReaperHarvest** is a powerful OSINT tool that checks where an email address is registered by probing known services.

---

## 🧠 Features

- 🔄 GitHub auto-update for services.json
- 🎭 Grim Reaper ASCII banner
- ❌ CAPTCHA-based services excluded (for now)
- ✅ Fast async scanning with colored output

---

## 📦 Installation

### 🔁 Option 1: Install directly from GitHub (recommended)

```bash
curl -o reaper https://raw.githubusercontent.com/TaoTheReaper/TheReaperHarvest/main/reaper
chmod +x reaper
sudo mv reaper /usr/local/bin/reaper
```

Make sure you also have this folder for data:

```bash
sudo mkdir -p /usr/local/share/reaper
```

And copy your `grim.txt` and `services.json` there.

---

### 💿 Option 2: Use `.deb` installer (for Debian-based systems)

Download and install:

```bash
sudo dpkg -i TheReaperHarvest.deb
```

---

## 🚀 Usage

```bash
reaper email@example.com
```

Output will be shown in your terminal with color-coded results:

- ✅ Registered
- ❌ Not Found
- ⚠ Error or forbidden
- 💥 Connection failed

---

## 🔄 How services update works

Every time `reaper` is launched, it fetches the latest `services.json` from your GitHub repo:

📡 [https://raw.githubusercontent.com/TaoTheReaper/TheReaperHarvest/main/services.json](https://raw.githubusercontent.com/TaoTheReaper/TheReaperHarvest/main/services.json)

This ensures you always probe the freshest service list.

---

## 📁 Repository structure

- `reaper` — main Python script
- `services.json` — list of services to probe
- `grim.txt` — ASCII banner
- `README.md` — documentation

---

## 🧪 Requirements

- Python 3
- aiohttp
- tqdm

Install them with:

```bash
pip3 install aiohttp tqdm
```

---

Made with ☠️ by **TaoTheReaper**
