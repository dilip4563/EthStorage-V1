EthStorage V1 Trusted Setup Ceremony – step by step  Guide


## Follow The Guide :

### Update & Install Dependencies
```
sudo apt update && sudo apt upgrade -y
sudo apt install -y curl git build-essential
```

### Install Node.js
```
curl -fsSL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install -y nodejs
sudo npm install -g npm@9.2
```

### Check Versions


```
node -v
npm -v
```

### Create Temporary Directory

```
mkdir ~/trusted-setup-tmp && cd ~/trusted-setup-tmp

```
### Install Phase2 CLI

```
sudo npm install -g @p0tion/phase2cli
```

### Verify CLI Installation


```
phase2cli --version
```

### Authenticate with GitHub

```
phase2cli auth
```

* Visit **[https://github.com/login/device](https://github.com/login/device)**
* Enter the code from your terminal
* Click **Authorize ethstorage**
* Allow **Read & Write access to GitHub Gists** in permissions

### 7) Start a `screen` session

```bash
screen -S ceremony
```

### 8) Join the ceremony

```bash
phase2cli contribute -c ethstorage-v1-trusted-setup-ceremony
```

* Press **Enter** for random input, or type your own characters.

---

## 🧹 Cleanup & Logout

When done, it’s recommended to clean up for security:

```bash
phase2cli clean
phase2cli logout
rm -rf ~/ceremonyeth
```

---

🖥 Screen Commands

| Action         | Command                       |
| -------------- | ------------------------------|
| Detach         | `Ctrl + A + D`                |
| Resume         | `screen -r ceremony`          |
| Delete screen  | `screen -XS ceremony quit`    |
| List sessions  | `screen -ls`                  |

---

## 🛠 Troubleshooting

**npm update error (`EBADENGINE`)**
You’re on Node 18 — stick to `npm@10`:

```bash
npm install -g npm@10
```

**Lost connection?**
Just re-run:

```bash
phase2cli contribute -c ethstorage-v1-trusted-setup-ceremony
```

It will resume from where you left off.


---

🎉 **You’ve successfully contributed to EthStorage’s decentralization!**

---

Follow : https://x.com/Web3Brothers for more tech contents.
