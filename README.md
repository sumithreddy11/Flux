 🔐 FLUX
        Secure CLI File Transfer in Go

   End-to-end encrypted file transfer built
   around AES-256-GCM + SHA-256 integrity checks.

        [ Go ] [ AES-256-GCM ] [ SHA-256 ]
        [ CLI ] [ HTTP ] [ Security Tests ]


It encrypts files locally using AES-256-GCM before uploading them to a server. The receiver downloads the encrypted payload, decrypts it, and verifies the resulting file using SHA-256.

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/01ef4786-50af-42d5-8765-851cbb067859" />

