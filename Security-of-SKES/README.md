# Security of symmetric-key encryption
#### Security Defination and adversary
* **Defination of Security of symmetric-key encryption** :
 * A Symmetric-key encryption is said to be secure if its semantically secure against a chosen-plaintext attack by a computionally bounded adversary 
 
* To break a Symmetric-key encryption scheme, the adversary has to accomplish the following:
 1. the adversary is given a challenge cipertext **c** 
 2. During the computation, the adversary can select the plaintext and obtain the corresponding ciphertext
 3. After a feasible amount of computation, the adversary obtain some infomation about the paintext corresponding to **c**  


* **Adversary's interaction**:
 * Passive attack:  
   * **Ciphertext attack** only  
    * **Known plaintxt attack** : the adversary also know some plaintext and the corresponding ciphertext
 * Active attack :
   * **Chosen-plaintext attack** : the adversary can also choose some plaintext and obtain the corresponding ciphertext 
    * **Chosen-ciphertext attack** : the adversary can also choose some ciphertext and obtain the corresponding plaintext
 * Other attack :
   * **Side channel attack**: monitor the encryption and decryption equipment (timing attacks, power analysis attacks, electromagnetic-radiation analysis, etc.)
    * **Physical attack**: bribery, blackmail, rubber hose, etc.

* **Computational power of adcersary**:  
 * **Information-theoretic security**:
   * adversary has infinite computational resource:
 * **Complexity-theoretic security** :
   * adversary is a 􏰄polynomial-time Turing machine􏰅.


* **Adversary's Goal** :
 1. Recover the secret key
 2. Systematically recover plaintext from ciphertext (without necessarily learning the secret key).
 3. Learn some partial information about the plaintext from the ciphertext (other than its length).

[A mathematical theory of communication](https://archive.org/details/bstj27-3-379)  

[Communication theory of secrecy systems](https://archive.org/details/bstj28-4-656)




