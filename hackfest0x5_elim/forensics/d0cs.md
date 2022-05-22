# d0cs

> docs have more functional,\
> *document bukan cuman sekedar untuk baca dan nulis\
> \
> Format Flag : `hackfest0x5{}`

A .dotm file provided, if we open the file it'll look like this\
\
![](https://i.imgur.com/uFyYjiz.png)\
\
Let's try changing the font color to any color\
\
![](https://i.imgur.com/ltkWb5M.png)\
\
It turned out that after changing the color it was just a decoy, after I checked again it turned out that there were Macros running on this document, let's see using the olevba tools, and the result will be like this:\
\
![](https://i.imgur.com/OcdTsmH.png)\
\
There are six variables that hold the Hex String, let's try to remove the character "ChrW()" and combine it to become a unified string.\
\
![image](https://user-images.githubusercontent.com/41176663/169695256-62ee1e22-33e3-4e13-af9c-24e105abb70f.png)\
\
And the result will be like this\
\
![image](https://user-images.githubusercontent.com/41176663/169695293-4eb484c6-a373-4de0-bcf2-5dbb10533711.png)\
\
We know that the string is in the form of a Hex string which is ascii codes, so we decode it from ascii code to string using an online converter.\
https://onlinestringtools.com/convert-ascii-to-string
\
![image](https://user-images.githubusercontent.com/41176663/169695374-3a859245-ea88-40fc-adea-7f4778e10b15.png)\
\
We will get base64 string \
`TG9yZW0gSXBzdW0gaXMgc2ltcGx5IGR1bW15IHRleHQgb2YgdGhlIHByaW50aW5nIGFuZCB0eXBlc2V0dGluZyBpbmR1c3RyeS4gTG9yZW0gSXBzdW0gaGFzIGJlZW4gdGhlIGluZHVzdHJ5J3Mgc3RhbmRhcmQgZHVtbXkgdGV4dCBldmVyIHNpbmNlIHRoZSBodHRwczovL3Bhc3RlYmluLmNvbS85YW5zQkxZSyBidXQgYWxzbyB0aGUgbGVhcCBpbnRvIGVsZWN0cm9uaWMgdHlwZXNldHRpbmcsIHJlbWFpbmluZyBlc3NlbnRpYWxseSB1bmNoYW5nZWQuIEl0IHdhcyBwb3B1bGFyaXNlZCBpbiB0aGUgMTk2MHMgd2l0aCB0aGUgcmVsZWFzZSBvZiBMZXRyYXNldCBzaGVldHMgY29udGFpbmluZw==`\
\
So we decode once again from base64 to string for readability, using the online converter https://www.base64decode.org/ and as a result we get a string\
`Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the https://pastebin.com/9ansBLYK but also the leap into electronic typesetting, remaining essentially unchanged. It was popularised in the 1960s with the release of Letraset sheets containing`\
there is a pastebin link, when we open the pastebin link\
![image](https://user-images.githubusercontent.com/41176663/169695520-22a56674-29be-4243-9dc9-9bcc59766d69.png)\
And great! we got the flag\
`hackfest0x5{de0bfuscatdd_shesss_678}`

