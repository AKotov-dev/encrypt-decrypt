**encrypt-decrypt** - a package of gpg files/folders encryption scripts for the Nemo, PCManFM, Dolphin and Caja context menus.

Dependencies: `zenity gnupg2 xsel tar zstd`

Creates the `Encrypt-Decrypt` item in the context menu of the Nemo, PCManFM, Dolphin and Caja file managers (MATE - via the shortcut in the `System` menu).

Encrypted files/folders get the extension `*.gpg` and are created/overwritten in the location directory of the main file. Decrypted files/folders are created/overwritten in the same place. On request, removes traces of encryption/decryption: clears the clipboard, recent files, and the input file/folder without the possibility of recovery (shred). Starting from v0.1-8, there is an indication of the encryption and cleanup progress. Localization of RU/EN.

**Important:** You can use, for example, one or more paragraphs from any book as a passphrase.

The length of the encryption password is selected experimentally and depends on the amount of RAM on the computer. With 8GB RAM, you can score a passphrase with a length of 10999 characters. The error appears on 11000: `gpg: Warning: using insecure memory!`. This indicates that there is not enough protected memory that gpg allocates for temporary storage of copies of the password. The passphrase is stored in protected memory and during calculations there are 2 or 3 copies (depending on the algorithm). Thus, if the passphrase is too long, the encrypted file will not be created.

In practice, this approach is very convenient for fast and reliable encryption of small files/folders containing important, personal information.

Tested in Mageia Linux-8 and LUbuntu-21.0.4.

![](https://github.com/AKotov-dev/encrypt-decrypt/blob/main/ScreenShots/encrypt-decrypt1.png)  ![](https://github.com/AKotov-dev/encrypt-decrypt/blob/main/ScreenShots/encrypt-decrypt2.png)  ![](https://github.com/AKotov-dev/encrypt-decrypt/blob/main/ScreenShots/encrypt-decrypt3.png)  ![](https://github.com/AKotov-dev/encrypt-decrypt/blob/main/ScreenShots/encrypt-decrypt4.png)
