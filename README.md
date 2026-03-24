# Secure Vault Service
 
A client-server application that allows organization members to securely store and share text files with guarantees of authenticity, integrity, and confidentiality.
 
Mutual authentication is established via X.509 certificates and the Station-to-Station (STS) protocol. All file content is encrypted client-side using AES-GCM before being sent to the server, meaning the server never has access to plaintext data. File sharing is handled through RSA-OAEP encryption of per-file AES keys, and group file access is managed by encrypting file keys individually for each member.
 
Supported operations: `add`, `read`, `list`, `share`, `replace`, `delete`, `revoke`, `details`, and full group management.
