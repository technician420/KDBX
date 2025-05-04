There should be 3 files uploaded on Github.
2025TS.kdbx
The purpose of this file is to store my personal information.

DiskEncrypt.kdbx
The purpose of this file is to store the keyfile required to unlock 2025TS.kdbx.
It also lets me practice typing the disk encryption password in the OS.

VCRescue20250503.zip
This is my Veracrypt rescue disk, it contains backups of my disk encryption keys.


My security/redundancy strategy is like this.
I memorize 2 passwords, lets call it PASS#1 and PASS#2.

2025TS.kdbx requires PASS#1 and a keyfile to unlock.
DiskEncrypt.kdbx only requires PASS#2 to unlock, but it contains the keyfile.
VCRescue20250503.zip requires PASS#2 to unlock.

Key Derivation Function:
I put a lot of thought into this. I use OSWAP standard Argon2d with 2 rounds, 19 MiB, and 1 thread.
The entropy of PASS#1 and PASS#2 exceeds 256 bits, so a light configuration for web authentication is sufficient.
