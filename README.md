#Secure E-Mail Communication System using Encryption Protocols

🔒 Project Overview

This project is a secure email simulation system built using Python.
It ensures that emails are confidential, tamper-proof, and readable only by the intended recipient.

The system uses a hybrid encryption model:

RSA (asymmetric encryption) → to encrypt the AES key

AES-GCM (symmetric encryption) → to encrypt the actual email message

This way, the project demonstrates how encryption ensures security in computer networks.

🎯 Features

User Registration: Each user gets a unique RSA key pair.

Send Message: Encrypts the message using AES and secures the AES key using recipient's RSA public key.

Inbox: List all received emails.

Read Message: Decrypt emails using the recipient's private key.

Secure Storage: Messages are stored encrypted in a local SQLite database.

⚙️ Technologies Used

Python 3.x

PyCryptodome (for RSA and AES encryption)

🔑 How Encryption Works

Sender: Generates a random AES key → encrypts message with AES-GCM → encrypts AES key with recipient's RSA public key.

Receiver: Uses their private RSA key to decrypt AES key → decrypts the message using AES-GCM.

✅ Sample Output

Register users → Alice, Bob

Alice sends message to Bob → [+] Message sent from 'Alice' to 'Bob' (encrypted)

Bob lists inbox → ID:1 | From:Alice | Subject:Meeting Update | Unread

Bob reads message → Decrypted message is displayed

🔮 Future Scope

Encrypt private keys with a password

Digital signatures for non-repudiation

GUI interface using Tkinter or web UI with Flask

SMTP/IMAP integration for real email sending

SQLite (for user and message storage)

Optional GUI: Tkinter/Flask (for future extension)
