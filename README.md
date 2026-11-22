# MTDataPro License Blacklist

This repository hosts the RSA-signed license blacklist file for MTDataPro.

The client software downloads `blacklist.dat`, verifies the RSA-2048 signature, and enforces:
- Serial number blacklist (revoked licenses stop working)
- Expiry date overrides (remote forced expiration)
- Machine code binding conflicts

The file is signed with the license signing key and cannot be forged.

## Update procedure
Run `blacklist_manage.ps1` on the signing machine, then push the updated `blacklist.dat` to this repository.
