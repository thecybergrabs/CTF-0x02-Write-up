### Salt is the important incrident

```
Doctor : Salt is important part of the food. Which one you use.
Me : Sir, I use salt of 0namak0 brand.
Doctor : Thats why you are facing issues today use 1337_Namak this is perfect to use.
Me : Sure sir.
Flag format: cybergrabs{}
Author: X3rz
```
##### Solution:
As in mentioned we get two interesting words `0namak0` and `1337_Namak`.

After unziping the file we got two images and a file named `...`

![image](https://github.com/thecybergrabs/CTF-0x02-Write-up/blob/main/Miscellaneous/Salt%20is%20the%20important%20incrident/1.png)

The file … contins MD5 hash 

The flag in the names of pictures is a fake flag.

so by running steghide on both of them without password gives you two files named `flag.pdf` and `-`

![image](https://github.com/thecybergrabs/CTF-0x02-Write-up/blob/main/Miscellaneous/Salt%20is%20the%20important%20incrident/2.png)

By looking at the contents of `-` we get:
```
Hint:
password_author
```
and PDF is password protected so as far we have:
```
MD5 hash 0namak0 and 1337_Namak A password protected pdf file.
```
So as the challange name states that these values are salts and by seeing MD5 its clear that it is salted MD5 hash with one of the available values.

So in the description  `Me : Sir, I use salt of 0namak0 brand.` So this leads to use this value first.

So finally we got: `07176f833cac2a1c539e86744fdcd4d7:0namak0`

Using `hashcat` we can crack this salted hash

`hashcat -m 10 hash.txt rockyou.txt` which gives `3205077273lunayoelareina` as password after cracking.

As in the `-` file the password of the pdf is password_author so we have `3205077273lunayoelareina` as password and `x3rz` author of this challenge.

Password of PDF: `3205077273lunayoelareina_x3rz`

By opening the file gives you the flag.

> *cybergrabs{Y0u_n4il3d_it_eW91bmFpbGVkaWl0}*
