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
### cryptography/Gene Encryption
discription:- Something related to genes ?
Flag is underscore separated with braces around it 
enc
solution:- at first i was struck for som time <br>
and then John [ctf-katana](https://github.com/JohnHammond/ctf-katana) helped me <br>
i made a [script](https://github.com/5h4rk-lab/CTF-tools/blob/master/dnafile.py) using this I got the flag.
![flag](https://github.com/N00BARMY/DarkCTF-Pre/blob/master/dna.png)
## flag:- darkCTF{darkCTFDeoxyribonucleicAcidCryptoxD}
### crypto/noMoreRemorse
discription:- Sometimes,what you see is not not what you get!!
quesiotn:- 
```
.-.-- .---- .---- .-..- --.-. ..-.. -...- ...-. ...-. ..... .---- --..- -..-- .-.-. --... -.-.- 
.--.- ..-.. ...-- ..... -...- ..--- ...-- ..-.. ...-. ..... --.-. .-.-- ..--- --... .---- ----. 
--... -.-.- ----. -.... ---.. ---.. ..-.- ---.. --..- -..--
```
solution:-
after spending some time i had remebred a CTF problem where we have to replace the bite <br>
then i had replaced `.` as 1 and `-` as 0:-
```
10100 10000 10000 10110 00101 11011 01110 11101 11101 11111 10000 00110 01100 10101 00111 01010 
10010 11011 11100 11111 01110 11000 11100 11011 11101 11111 00101 10100 11000 00111 10000 00001 
00111 01010 00001 01111 00011 00011 11010 00011 00110 01100 
```
converting this baudot using baudot decoder on decode.fr I got:-
```
HTTPS://TINYURL.COM/SHOUTEUREKAAGAIN
```
which further gives you a weird text <br>
```
hｔtpｓ：//іmgur．сοｍ/a／d2ｈhｄHlνｄＸNｚWlｚd2hｈｄHｌvｄＷdldC5５b３ｖqdΧＮ0bmVlZΗRvϹ２VｌｂGｌrＺΧＲoҮＸＲrZWVwdH
```
Then i had decoded this message was encrypted using special encryption called twitter secreat measages <br>
which can be decoded using this [tool](https://holloway.nz/steg/). <br>
further following the decoded message you will get your flag. <br>
![flag](https://github.com/N00BARMY/DarkCTF-Pre/blob/master/twiter.png)
### crypto/'m&m' 
desc:- You know your Morse Code?
question:-
```
--... -.... ..... .---- --... ---.. ..... ---.. ..... -.... ..--- ....- --... ---.. ..--- ...-- ...-- ..--- ..... -.... ....- -.... -.... ....- ...-- ..--- ...-- ---.. ...-- ...-- .---- --... ---.. ....- -.... ....- ---..
```
after decodeing the morse code you would get
```
7651785856247823325646643238331784648
```
this is a [morbit cipher](https://www.dcode.fr/morbit-cipher)
but this needed a key so just make a script and bruteforce script.
```
decoded_morse = "7651785856247823325646643238331784648"

from itertools import permutations

MORSE_CODE_DICT = {'..-': 'U', '--..--': ', ', '....-': '4', '.....': '5', '-...': 'B', '-..-': 'X', '.-.': 'R', '--.-': 'Q', '--..': 'Z', '.--': 'W', '-..-.': '/', '..---': '2', '.-': 'A', '..': 'I', '-.-.': 'C', '..-.': 'F', '---': 'O', '-.--': 'Y', '-': 'T', '.': 'E', '.-..': 'L', '...': 'S', '-.--.-': ')', '..--..': '?', '.----': '1', '-----': '0', '-.-': 'K', '-..': 'D', '----.': '9', '-....': '6', '.---': 'J', '.--.': 'P', '.-.-.-': '.', '-.--.': '(', '--': 'M', '-.': 'N', '....': 'H', '---..': '8', '...-': 'V', '--...': '7', '--.': 'G', '...--': '3', '-....-': '-', '\n' : ' '}
MORBIT = ['..', '.-', '. ', '-.', '--', '- ', ' .', ' -', '  ']

def morse(ciphertxt,flag=None): 
    plaintxt = ''
    for word in ciphertxt.strip().split("  "):
        for c in word.strip().split(" "):
            if c in MORSE_CODE_DICT:
                plaintxt += MORSE_CODE_DICT[c]
            else:
                pass
        plaintxt += ' '
    return plaintxt
    
def morbit(ciphertxt,flag=None):
    if flag==None:
        flag=""
    scores=[]
    for p in permutations('0123456789'):
        MORBIT_CODE_DICT = dict(zip(p, MORBIT))
        morsetxt = ""
        for c in ciphertxt:
            if c in MORBIT_CODE_DICT:
                morsetxt += MORBIT_CODE_DICT[c]
        if flag in morse(morsetxt,flag):    
        	print(morse(morsetxt,flag))
        
morbit(decoded_morse,"DARKCTF")
```
Running this script will give you the flag (key = 555542069)

## Flag :- darkCTF{MORSE_2_MORBIT}
