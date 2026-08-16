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
 1.AES-256-GCM authenticated encryption
 2.Ciphertext tamper detection
 3.Wrong-key rejection
 4.#️SHA-256 integrity verification
 5.Encrypted file upload/download
 6.Unique transfer IDs
 7.Self-describing transfer metadata
 8.Transfer status tracking
 9.Command-line sender and receiver
 10.HTTP-based transfer server
 11.Automated security tests
 12.Stream-based encryption for file transfers
---
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



