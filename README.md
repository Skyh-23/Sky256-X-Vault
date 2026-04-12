# 🔐 Sky256X Vault

A **client-side encryption app** that securely encrypts and decrypts text and files directly in the browser using modern cryptography.

---

## 🚀 Features

- 🔒 AES-256-GCM encryption (secure & authenticated)
- 🔑 Password + 256-bit access key protection
- 📦 Supports any file type (images, videos, docs, etc.)
- ⚡ Chunked encryption (handles large files efficiently)
- 🌐 Fully client-side (no server upload)
- 🧠 Random salt + nonce for every encryption
- 🔁 Same input → different encrypted output every time

---

## 🧩 How It Works

### Encryption Flow
  Password + Access Key → PBKDF2 → AES Key
  File/Text → AES-256-GCM → Encrypted Package (.sky256x2)


### Decryption Flow
  Password + Access Key → PBKDF2 → AES Key 
  Encrypted Package → Decrypt → Original Data


---

## 📦 File Format (.sky256x2)

Each encrypted file contains:
- Header (metadata: name, type, size, version)
- Salt (for key derivation)
- Nonce (for AES-GCM)
- Chunked encrypted data
- Authentication tag (integrity check)

---

## 🔐 Security Model

- Uses **AES-256-GCM** for strong encryption
- Uses **PBKDF2 (600,000 iterations)** to resist brute-force attacks
- Every encryption uses:
  - Random salt
  - Random nonce
- Integrity protected via AES-GCM authentication

> ⚠️ Security depends on **strong password + access key**

---

## 🧠 Key Concept

- Each file requires:
  - Password 🔑
  - 256-bit Access Key 🧬
- Without both → decryption fails

---

## 📱 Build as App

### APK (Android)
1. Host project (GitHub Pages / Netlify / Cloudflare)
2. Use **PWABuilder**
3. Generate APK

### EXE (Windows)
1. Use **Electron**
2. Package using `electron-builder`
3. Build `.exe`

---

## 🛠 Tech Stack

- HTML, CSS, JavaScript
- WebCrypto API
- AES-256-GCM
- PBKDF2-SHA256

---

## ⚠️ Important Notes

- This is **client-side encryption only**
- No data is uploaded anywhere
- Lost password or access key = **data unrecoverable**

---

## 📌 Future Improvements

- Argon2 support (better than PBKDF2)
- UI/UX enhancements
- Mobile optimization
- Optional key recovery system

---

## 🏁 License

This project is for educational and personal use.

---

## 👨‍💻 Author

**Hiren Sumra**
