# DarkCTF-Pre-

## Crypto writeups:-

### Cryptography/Really Secure Algo:-
Author:- karma
```
n = 977777777777777777777777777777777777777777777777777777777777777777777777
777777777777777777777777777777777777777777777777777777777777777777777
e = 65537
c = 777100860344719251862233099079929815950590358671816920785821983126
256200182002548130383416252558510764139287733939898022176140368825482344800
```
Solution:-
This is a message encrypted in RSA (Rivest, Shamir, Adleman) form. There is <br>
a great tool for solving RSA named [RsaCtfTool](https://github.com/Ganapati/RsaCtfTool) <br>
so using this tool i got the flag. <br>
usage of tool:-
```
python3 RsaCtfTool.py -n 977777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777777 -e 65537 --uncipher 777100860344719251862233099079929815950590358671816920785821983126256200182002548130383416252558510764139287733939898022176140368825482344800
```
## flag:- "darkCTF{CTF_without_rsa?_pttf}"
### Cryptography/Find Fish
Author: - karma
```
xxkxxxxkxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxcdddcxxxxxxxxxxxxxxxxxc
dddddddcddddddddddddddddddddddddddddddddddddddddcxxxxxxxxxxxxxxxxxc
ddddddddddddddcxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
xcddddddddddddddddddddddddddddddddddddcxxxxxxxxxxxxxxcxxxxxxxcddddd
ddddcdddddddddddddddddddddddddddddddddddddddddddddddddddcxxxxxxxxxx
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxcddddddddddddddd
dddddddddddddddddddddddddddddddddddddddddddcxxxxxxxxxxxxxxxxxxxxxxx
xxxxxxxxxxxxxxxxxxxxxcdddddddddddcddddddddddddddddddddddddddddddddd
dddcxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxcddddddddddddddd
ddddddddddddcddddddddddddddddcxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
xxxxxxxxxxxxxxxxxxxxxxxxxcdddddddcddddddddddddddddddddddddddddddddd
ddddddddddddddddddddddcxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
xxxxxxxxxxxxxxxxxxcdddddcxxxxxxxxxxxxcddddddddddddddddddddddcxxxxxx
xxxxxxxxxxxcddddddddddddddcxxxxxxxxxxxxxxxxxxxxxxxc
```
solution:-
This is a dead fish cipher using tool [deadfish decoder](https://www.dcode.fr/deadfish-language) <br>
we can easyly decode it.
![dead_fish](https://github.com/N00BARMY/DarkCTF-Pre/blob/master/deadfish.png)
## flag:- "darkCTF{Welc0m3_T0_D4rk4rmyctf}"
### Cryptography/Orange Text
Author:- kick
solution:-
Orange is rich with C vitamin and if you think deeper you will get to know there is a <br>
citric cipher. So using citric cipher decoder just decrypt the text and flag is yours.<br>
![orange](https://github.com/N00BARMY/DarkCTF-Pre/blob/master/orange.png)
## flag:- darkCTF{us1ng_th1s_typ3_is_br34k4b13}
