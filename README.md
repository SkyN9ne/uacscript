# UAC Bypass Vulnerability in Windows Script Host

The Windows Script Host executable `wscript.exe` suffer from a vulnerability due to a missing embedded manifest.
_Using another exploit, the combination of `wusa.exe` and `makecab.exe` files can be copied to the Windows directory (`%WINDIR%`)._ 
Copies of a manifest and the script host allow to execute the copied script host and bypass UAC warning messages in case UAC settings are default. 

Both ZDI and Microsoft are aware of this issue, expectedly ZDI didn't accept the admission because it's not a remote vulnerability. Surprisingly Microsoft didn't accept the vulnerability because "UAC isn't considered a security boundary".

Only Windows 7 is confirmed vulnerable, Windows 8 has a embedded manifest and Windows 10 is untested.
