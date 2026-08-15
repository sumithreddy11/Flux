# Flux
Flux is a secure command-line file transfer system written in Go.  It encrypts files locally using AES-256-GCM before uploading them to a server. The receiver downloads the encrypted payload, decrypts it, and verifies the resulting file using SHA-256.
