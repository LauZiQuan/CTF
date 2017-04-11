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
