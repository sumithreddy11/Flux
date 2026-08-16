# 🔐 Flux

### Secure Command-Line File Transfer in Go

Flux is a security-focused command-line file transfer system written in Go.

It encrypts files **before they leave the sender** using **AES-256-GCM**, transfers only the encrypted payload through the server, and verifies the decrypted file using **SHA-256 integrity verification**.

> **Plaintext stays on the sender and receiver. The server stores encrypted data.**

<p align="center">

**Go • AES-256-GCM • SHA-256 • HTTP • CLI**

</p>

---

## ✨ Why Flux?

Traditional file-transfer systems often rely on the server to handle or temporarily store plaintext files.

The server does not need the encryption key to store and transfer the encrypted file.
Flux takes a different approach:

```text
                         FLUX

        SENDER                              RECEIVER
          │                                    ▲
          │                                    │
       File                               Encrypted File
          │                                    │
          ▼                                    │
      SHA-256                                  │
          │                                    │
          ▼                                    │
   AES-256-GCM Encrypt                         │
          │                                    │
          ▼                                    │
   Encrypted Payload                           │
          │                                    │
          └──────────────► SERVER ─────────────┘
                           │
                           │
                    Stores encrypted
                    payload + metadata

##🚀 Features
🔐 AES-256-GCM authenticated encryption
🛡️ Ciphertext tamper detection
🔑 Wrong-key rejection
#️⃣ SHA-256 integrity verification
📦 Encrypted file upload/download
🆔 Unique transfer IDs
📋 Self-describing transfer metadata
🔄 Transfer status tracking
💻 Command-line sender and receiver
🌐 HTTP-based transfer server
🧪 Automated security tests
⚡ Stream-based encryption for file transfers

## Architectureflux/
│
├── cmd/
│   │
│   ├── flux/
│   │   ├── main.go
│   │   └── main_test.go
│   │
│   └── server/
│       └── main.go
│
├── internal/
│   │
│   ├── crypto/
│   │   ├── encrypt.go
│   │   ├── hash.go
│   │   ├── stream.go
│   │   ├── encrypt_test.go
│   │   └── stream_test.go
│   │
│   ├── network/
│   │   └── server.go
│   │
│   ├── storage/
│   │   └── ...
│   │
│   └── transfer/
│       ├── create.go
│       ├── create_test.go
│       ├── manager.go
│       └── metadata.go
│
├── .gitignore
├── go.mod
└── README.mde



