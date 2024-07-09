# Usage.md

## Notes

* Git-Bash MINGW64 terminal does not support "prompt", so use PowerShell or WezTerm terminal.
* In Windows-Subsystem-for-Linux, git uses "credential.helper" and "credential.credentialStore" from Host Windows-OS.
* HDD/CD-ROM/PSD/Pendrive/SSHFS Partitions:
  * Computer Hard-Disk-Drive(HDD)/CD-ROM Partitions: C, D, E, F, G, H, I, J
  * Portable-Storage-Device(PSD)/Pendrive Partitions: K, L, M, N, O, P, Q
  * SSH-File-System(SSHFS)/Network/Other-Computer Partitions: R, S, T, U, V, W, X, Y, Z

## Google Sheet

* If google-sheet's returned result does not show "date" field properly, then select column and change data format from "Automatic" to "Plain text".

## Charmbracelet-Gum

* In Charmbracelet-Gum textarea, do not use Keyboard-Enter / Line-Feed (LF) / Carriage-Return-Line-Feed (CRLF), because it breaks Curl code, instead use '\n' character.

## Known Problems

* Date stores correctly, but does not show properly when get from api. Use this format "01-01-2000D" OR "01-01-2000D12:24:48".
