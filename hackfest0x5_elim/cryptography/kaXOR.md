# kaXOR

> Just EZ chall, and I know u can do it!\
> \
> Format Flag : hackfest0x5{}

Provided chall with a python file and cipher text that must be decrypted


```py
from secret import flag, key

cipher = ''
for i in range(len(flag)):
    cipher += chr(ord(flag[i]) ^ key)
    
a = open('cipher.txt', 'w')
a.write(cipher)
a.close()
```
It can be seen that the key is only 1 letter because the python file is written (^ key) instead of (^ key[x]). Here I use a PHP script from the previous CCUG documentation\
```php
<?php
$cipher = file_get_contents("cipher.txt");
$decx = "";
for ($i=0; $i < 255; $i++) {
$dec = "";
for ($j=0; $j < strlen($cipher); $j++) {
  $dec .= chr(ord($cipher[$j]) ^ $i);
  }
$decX .= "$dec\nxx\n";
}
file_put_contents("a.txt", $decX);
```
After the script is run, the results that have been decrypted will be entered into an a.txt file, like this:\
![image](https://user-images.githubusercontent.com/41176663/169957952-e7682175-8192-4959-9c7a-0ca30c8f0d70.png)\
\
Let's try CTRL + F to find the flag string with the prefix "hackfest"\
![image](https://user-images.githubusercontent.com/41176663/169958131-08629191-f156-4d0d-9626-61166c4413ba.png)\
\
And the flag is `hackfest0x5{bRu73F0rC3_i5_th3_R1gh7_4nSweR_f0R_th1S_Ch4l1enG3}`
