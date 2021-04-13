### Somethinf Feasy
```
Key to unlock anything is already with you.
Flag format: cybergrabs{}
Author: Odin
```

##### Solution:

```Challenge file:
Cipher =>  O|k.Wa{.]{|k.Wa{.[}kj.Ma||kmz.Ekw.4.P*-PP(---*(*-*(/P(((+h(N-$P$(PPhPh-P-PNh-(P*(/PoP--&-(Pj(N-*NhPo-+(&P-P&P--PP(-&(/-*P+Nl
```
In this challenge first you got the file. It has Encrypted text and as its description says `Key to unlock anything is already with you.`

So if u apply Xor decryption on it you with the key as key you can get the decrypted text like this:

```
Are You Sure You Used Correct Key : ^$#^^&###$&$#$&!^&&&%f&@#*^*&^^f^f#^#^@f#&^$&!^a^##(#&^d&@#$@f^a#%&(^#^(^##^^&#(&!#$^%@b
```

##### Hint: Remember your keyboard is your true friend & ot will help you two times in this journey.
So if you look at the keyboard you will get that it was alphanumberic Characters you have to replace them by digits.

```
s = "^$#^^&###$&$#$&!^&&&%f&@#*^*&^^f^f#^#^@f#&^$&!^a^##(#&^d&@#$@f^a#%&(^#^(^##^^&#(&!#$^%@b"
l = len(s)


i = 0

while i<l:
    if(s[i] == '!'):
        print("1" , end='')
    elif(s[i] == '@'):
        print("2", end='')
    elif(s[i] == '#'):
        print("3", end='')
    elif(s[i] == '$'):
        print("4", end='')
    elif(s[i] == '%'):
        print("5", end='')
    elif(s[i] == '^'):
        print("6", end='')
    elif(s[i] == '&'):
        print("7", end='')
    elif(s[i] == '*'):
        print("8", end='')
    elif(s[i] == '('):
        print("9", end='')
    elif(s[i] == ')'):
        print("0", end='')
    else:
        print(s[i], end='')

    i = i+1
```
    
Script by Odin.

After Running this script you will get the hex value:

```
643667333474347167775f723868766f6f36362f3764716a6339376d72342f6a35796369633667397134652b
```
After Decode it online you will get the another Encoded Cipher.

```
d6g34t4qgw_r8hvoo66/7dqjc97mr4/j5ycic6g9q4e+
```
Now if you remeber the hint we need keyboard once again so basically it was a Keyboard Shift Cipher after Decoding it you will get:

`cybergrabs{fin4llyy0ucam3ou7fr0mth3k3yboard}`

Seperate each Word By _ and you have your final flag.

> *cybergrabs{fin4lly_y0u_cam3_ou7_fr0m_th3_k3yboard}*
