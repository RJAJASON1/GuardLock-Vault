# 🔐 GuardLock Vault

**GuardLock Vault** is a secure, terminal-based password and file protection system designed to safely store, encrypt, export, and manage sensitive data using strong cryptography.

It provides a simple menu-driven interface while enforcing strict encryption rules to protect your data from unauthorized access.

---

## ✨ Features

- 🔑 **Lock Code–Based Security**
  - All data is protected using a user-defined lock code.
  - Encryption keys are derived using **PBKDF2 + SHA-256** with a high iteration count.

- 🔒 **Encrypted Password Storage**
  - Store passwords securely in an encrypted vault.
  - Passwords can be hashed multiple times before storage.

- 👁️ **View Encrypted Data Securely**
  - View stored passwords only after successful decryption.
  - View locked files without permanently decrypting them.

- 📁 **Secure Files**
  - Lock any text-based file into an encrypted `.locked` file. Only text files (.txt)
  - Original files are deleted after being secured.

- 📤 **Export Decrypted Data**
  - Export encrypted password files into **plain text** when needed.
  - Exported files are placed automatically into the `data/exports` folder.

- 🔄 **Reset Lock Code**
  - Change your lock code while preserving encrypted data.
  - Data is decrypted in memory and re-encrypted securely.
  - No plaintext is ever written to disk during the reset process.

- 🧹 **System Reset**
  - Completely wipe all stored data and encrypted files.

- 🔐 **Strong Cryptography**
  - Uses AES-based Fernet encryption
  - PBKDF2HMAC with 390,000 iterations
  - Random per-file salt

---

## 🗂️ Folder Structure

```
GuardLock_Vault/
├── data/
│   ├── passwordprotected/
│   │   └── hashed_passwords.txt
│   ├── securedpasswordslist/
│   │   └── *.locked
│   └── exports/
│       └── *_decrypted.txt
├── GuardLock_Vault.py
└── README.md
```

---

## 🚀 How to Run

### Run with Python
```bash
python GuardLock_Vault.py
```

### Run as Executable
Double-click the executable or run it from Command Prompt:
```bat
GuardLockVault.exe
```

---

## 🔐 Security Notes

- Encrypted files cannot be decrypted without the correct lock code.
- Files opened on other systems (Linux/Kali) appear as unreadable binary data.
- Decryption logic exists only inside GuardLock Vault.
- No encryption keys are stored on disk.

⚠️ If the lock code is permanently lost, encrypted data cannot be recovered.

---

## 🛠 Dependencies

- Python 3.9+
- cryptography

Install dependency:
```bash
pip install cryptography
```

---

## 📌 Disclaimer

GuardLock Vault is intended for securing sensitive files, passwords and other data.
Always back up important data before resetting or erasing the system.
Do not view or modify any encrypted files as they might get corrupted or lost.
When terminating GuardLock Vault, possible errors might show and the application closes. 
These errors are not related to the application and they are errors from a tool i use to convert it to an executable. 
So don't get worry about your data. Everything is safe and secure. 🛡️🔐