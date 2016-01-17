# Block Cipher

#### Steam Ciphers
* Defination:
  * A steam cipher is a symmetric-key encryption scheme in which each successive character of plaintext determines a single character of ciphertext
* Example:
  * Substitution cipher
  * Vigenere cipher
  * One-time pad
  * Enigema

![alt text][logo]
[logo]: http://www.webbasedprogramming.com/Java-Expert-Solutions/f27-2.gif

#### Block Ciphers
* Defination:
  * A block cipher is a symmetric-key encryption scheme in which a fixed-length block of plaintext determines an equal-sized block of ciphertext
* Example:
  * DES
  * AES

![alt text][logo2]
[logo2]: http://imps.mcmaster.ca/courses/SE-4C03-07/wiki/mccombi/blockcipherencrypt.png

#### Data Encryption Standard (DES)
* Overview of DES:
  * Block cipher with 64-bit block, 56-bit key, and 16 rounds of operation
  * Basically, DES is (believed to be) secure against everything except brute-force key search
    * Brute-force attacks : try every key
  * **Mulptiple encryption**:
    * Re-encrypt the ciphertext one or more times using independent keys, and hope that this operation increases the effective key length.
    * Multipe encryption does not always increas security.
  * Double encryption:
    * Attack on Double-DES:
    Main ideal: Meet-in-the-middle  
    [Wikipedia](https://en.wikipedia.org/wiki/Meet-in-the-middle_attack)

![alt text][double DES]
[double DES]: http://image.slidesharecdn.com/des-140619083232-phpapp02/95/des-49-638.jpg?cb=1403167377

#### The Feistel network design
* Components of Festel cipher:
  * Parameters: n(half the block length), h(number of rouonds), l (key size).
  * M = {0,1}(2n), C = {0,1}(2n), K = {0,1}(l)
  * A key **scheduling algorithm** which determines subkeys k1, k2, ....,kh from a key k.
  * Each subkey ki defines a component function:
    * fi: {0,1}(n) -> {0,1}(n)
  * **Encryption** take h round:
    * Round 1: (m0,m1)->(m1,m2), where m2 = m0 + f1(m1).
    * Round 2: (m1,m2)->(m2,m3), where m3 = m1 + f1(m2).
    * .....
    * Round h: (mh-1,mh)->(mh,mh+1), where mh+1 = mh-1 + f1(mh).
    * Ciphertext is c = (mh,mh+1)
  * *Decryption**: Given c = (mh,mh+1) and k, to find m =(m0,m1):
    * Compute mh-1 = mh+1 + fh(mh)
    * Similarly, compute mh-2,...,m1,m0
* Feistel cipher with n = 32, h =16, l = 56 is DES
* Initial permutation

![alt text][initial p]
[initial p]: https://upload.wikimedia.org/wikipedia/commons/thumb/1/12/DES-ip.svg/800px-DES-ip.svg.png 

* Key schedduling algorithm

![alt text][key scheduling]
[key scheduling]: https://upload.wikimedia.org/wikipedia/commons/thumb/6/6a/DES-main-network.png/500px-DES-main-network.png  

* DES S-box

![alt text][s-box]
[s-box]: https://upload.wikimedia.org/wikipedia/commons/4/44/DES_S-box.jpg












