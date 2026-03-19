# 🔐 GuardLock Vault

**GuardLock Vault** is a secure, terminal-based password and file protection system designed to safely store, encrypt, export, and manage sensitive data using strong cryptography.

It provides a simple menu-driven interface while enforcing strict encryption rules to protect your data from unauthorized access.

---

## ✨ Features

- 🔑 **Lock Code–Based Security**
  - All data is protected using a user-defined lock code.

- 🔒 **Encrypted Password Storage**
  - Store passwords securely in an encrypted vault.
  - Passwords can be hashed multiple times before storage.

- 👁️ **View Encrypted Data Securely**
  - View stored passwords only after successful decryption.
  - View locked files without permanently decrypting them.

- 📁 **Secure Files**
  - Lock any type of file into an encrypted `.locked` file.
  - Original files are deleted after being secured.

- 📤 **Export Decrypted Data**
  - Export encrypted password files into **plain text** when needed.
  - Exported files are placed automatically into the Desktop.

- 🧹 **System Reset**
  - Completely wipe all stored data and encrypted files.

- 🔐 **Strong Cryptography**
  - Uses AES-based Fernet encryption
  - PBKDF2HMAC with 390,000 iterations

---

## 🔐 Security Notes

- Encrypted files cannot be decrypted without the correct lock code.
- Files opened on other systems (Linux/Kali) appear as unreadable binary data.
- Decryption logic exists only inside GuardLock Vault.
- No encryption keys are stored on disk.

⚠️ If the lock code is permanently lost, encrypted data cannot be recovered.

---

## 📌 Disclaimer

GuardLock Vault is intended for securing sensitive files, passwords and other data.
Always back up important data before resetting or erasing the system.
Do not view or modify any encrypted files as they might get corrupted or lost.
When terminating GuardLock Vault, possible errors might show and the application closes. 
These errors are not related to the application and they are errors from a tool i use to convert it to an executable. 
So don't get worry about your data. Everything is safe and secure. 🛡️🔐
