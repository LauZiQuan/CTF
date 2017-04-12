## Pico CTF Writeup

The CTF can be found on https://2017game.picoctf.com

### level 1 
#### FORENSICS - Digital Camouflage
The mission is to find the password from a data.pcap
Tools Used: Wireshark

1) From Wireshark, I view the conversation for the TCP stream, and you will find something interesting. 
2) OFBGRW8wdHRIUQ%3D%3D is the user password. But it is encrypted. The %3D is the html representation for "=" as such we only need to decrypt the OFBGRW8wdHRIUQ. 
3) Using Base64 Decryption, you are able to get the answer "8PFEo0ttHQ".

#### FORENSICS - Special Agent User
The mission is to identify the User Agent and provide the version.
Tools Used: Wireshark

1) Using Wireshark, similiar you can look for the TCP Stream and Identify the User Agent
2) A particular stream have some interesting results which consist for certain Browser Information
3) Copy Paste the Browser Information in the particular Format and that is your flag. 

#### CRYPTOGRAPHY - keyz
The mission is to generate the SSH Keys and login using SSH. 
Tools Used: PUTTYGEN and PUTTY (Windows)

1) Download the tools
2) Generate the Public Key and Private Key. 
3) Access the webshell on pico and copy in the SSH Public Course 
4) Afterwhich, access the SSH using Putty and the flag will be found once you login. 

#### CRYPTOGRAPHY - Substitute
The mission is to get the flag by decoding the cipher text
Tools Used: ~

1) The Mission name already told use that it is a Substitute Cipher.
2) Just google for a tool and you are able to find the flag easily. 

#### CRYPTOGRAPHY - Hash 101
The mission is to get the flag by decoding the cipher text
Tools Used: ~

1) nc to the shell2017.picoctf.com 9661
2) You are given 4 Task
3) First Task is to decode the binary to text
4) Just throw the values into a binary convert and you get the word. 
5) Second Task is Converting the text to Hex and then Decimal.
6) Third Task is to provide a Hash That results in nth Number
7) Using Ascii to determine the values 
8) The final Task is the crack the given code with MD5 hash.

#### CRYPTOGRAPHY - computeAES
The mission is to get the flag by decoding AES ECB Mode
Tools Used: ~

1) With the Given Cipher Text and Key, I need to decrypt the ciphertext to get the plain text. 
2) Next thing i know is that there is a Base64 Encryption.
Encrypted with AES in ECB mode. All values base64 encoded
ciphertext = V3Vqirostg6qW26sle5mnyrwEYSrteN6oHkilO50e9dFkN+0JhC3yu0LcQNw/hXU
key = r7y1dhmTvjQrcra7A1UQFw==
3) 




#### MISC - Internet Kitties
The mission is to get service by using nc
Tools Used: ~

1) Just nc into the port to get the flag


#### MISC - Leaf of the Tree
The mission is to get the flag using ls and cat
Tools Used: ~

1) using cd and Ls to check the for the flag
2) once the flag is found, use the cat to print the flag.

#### MISC - Leaf of the Tree
The mission is to get the flag using ls and cat
Tools Used: ~

1) Find command
2) find /problem/long_dir_name_here -name "flag"
