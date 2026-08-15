                    🔐 FLUX
        Secure CLI File Transfer in Go

   End-to-end encrypted file transfer built
   around AES-256-GCM + SHA-256 integrity checks.

        [ Go ] [ AES-256-GCM ] [ SHA-256 ]
        [ CLI ] [ HTTP ] [ Security Tests ]

------------------------------------------------------------

                    🚀 WHY FLUX?

     Send files without giving the server access
                    to plaintext data.

             Sender                  Receiver
               │                        ▲
               ▼                        │
            SHA-256                     │
               │                        │
               ▼                        │
          AES-256-GCM                   │
               │                        │
               ▼                        │
        Encrypted Payload ──► Server ──┘
                              │
                              ▼
                         Stored Ciphertext

------------------------------------------------------------

                    🔒 SECURITY

  ✓ AES-256-GCM authenticated encryption
  ✓ Tamper detection
  ✓ Wrong-key rejection
  ✓ SHA-256 integrity verification
  ✓ Encryption happens before upload
  ✓ Server stores encrypted payload

------------------------------------------------------------

                    ⚡ QUICK START

  # Start server
  go run ./cmd/server

  # Send
  go run ./cmd/flux send photo.jpg

  # Receive
  go run ./cmd/flux receive <transfer-id> <key>

------------------------------------------------------------

                 🧪 SECURITY TESTING

  go test ./...

  ✓ Encryption/decryption
  ✓ Stream encryption
  ✓ Tampered ciphertext
  ✓ Wrong encryption key
  ✓ SHA-256 mismatch
  ✓ Transfer metadata

------------------------------------------------------------

                  🏗 ARCHITECTURE

              cmd/
             /    \
          flux    server
           │        │
           ▼        ▼
        crypto   network
           │        │
           └──► transfer
                    │
                    ▼
                 storage

------------------------------------------------------------

                    🗺 ROADMAP

  ✓ Single-file transfers
  ✓ Encryption
  ✓ Integrity verification
  ✓ Metadata
  ✓ CLI
  ✓ HTTP server

  → Resumable transfers
  → Multi-file transfers
  → Progress tracking
  → Authentication
  → Expiring transfers
  → Web interface

------------------------------------------------------------

              Built with Go • Security-first
                  

   


<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/01ef4786-50af-42d5-8765-851cbb067859" />

