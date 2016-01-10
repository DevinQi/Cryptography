# Symmetric-Key-Encryption-scheme
* **Defination**:  
  A Symmetric-key encryption scheme consist of:
  * M - the Plaintext space
  * C - the Ciphertext space
  * K - the Key space
  * a family of encryption function,E:M->C, for all k ∈ K
  * a family of decryption function,D:c->M, for all k ∈ K     
such that D((E(m)) = m for all m ∈ M,k ∈ K  

* **The simple substitution cipher**:  
  * Defination:
    * a substitution cipher is a method of encoding by which **units** of plaintext are replaced with ciphertext, according to a fixed system; the "units" may be single letters (the most common), pairs of letters, triplets of letters, mixtures of the above, and so forth.
  * Example:  
  
  |Key| A | B | C | D | E | F | G | H | I | G | K | L | M | N | O | P | Q | R | S | T | U | V | W | X | Y | Z |  
  |---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|  
  | A | D | N | X | E | S | K | O | G | T | A | F | P | Y | I | Q | U | B | I | Z | G | V | C | H | W | M | L |  
  

         m = THE BIG DOG   ========> GJS NTO EQO  
  * Breaking the substitution cipher
      * All Letter Are not **Equally** in English Text, some letter like "E" is more likely to appear
      * Using the frequency in [WikiPedia](https://en.wikipedia.org/wiki/Letter_frequency) ,we can determine the plaintext using only the ciphertext
      * Also, there is a website called [Black Chamber](http://www.simonsingh.net/The_Black_Chamber/crackingsubstitution.html) can help us
* **Polyalphabetic cipher**
  * Basic ideal:  
    * Use several permutations, so a plaintext is encrypted to one of several possible ciphertext letter.
  * **Vingenere cipher**:  
    * Key is an English letter which has no repeated lettes. e.g. k =CRYPTO
    * Example of encryption:  
    
| M | t | h | i | s | i | s | a | m | e | s | s | a | g | e |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|Key| C | R | Y | P | T | O | C | R | Y | P | T | O | C | R |
| c | V | Y | G | H | B | G | C | D | C | H | L | O | I | V |  

  * Here A = 0, ...., Z = 25, addition and mod 26
    * Decryption is substribution and mod 26
  * Vingenere cipher is good but also can be break:
    * There are two steps to break it:  
      1. Find the key length l:
        * Make a guess for l (usually start from 2)
        * Divids the ciphertext in to l group, Examine the frequency distribution of letters in each group
        * If eah distributions "looks like" expected distribution of letter from sensible English text,the length is probably right 
      2. Determine each letter of the key:
        * Notice that the each letters in each group were obtained by applying a permutation that is cycily shift the alphabet to the corresponding plaintext letter.
        * Using the frequancy counts of ciphertext in each group to make a guess of ith key word of the key
        * Check your keyword by decryption your ciphertext
    * Online tool [here](http://www.simonsingh.net/The_Black_Chamber/vigenere_cracking_tool.html)
    * My c++ [code]()
* The one-time pad
  * The one-time pad is modified vision of Vingenere cipher:
    * Key is random string of letter which has same length with plaintext
  * Re-use of one-time pad:
    * re-use of one-time pad may cause leak of infomation:
    * if c1 = m1 + k, c2 = m2 + k , then c1 -c2 = m1 - m2, if m1 knowd ,m2 can be easily computed
  * One-time is perfectly secure but there is no method to achieve this, thus its useless in pratice










