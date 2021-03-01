# Message Encryption
**Project developed in Assembly language, MIPS64 Architecture**

## About the project

The project meets the following requirements:
* <div align="justify"> For a number *p* it is desired to determine the generator (smallest) *g* so that this generator, successively raised to power, modulo *p*, generates all the elements from 1 to *p* - 1.
* Given a clear message, to encrypt.
* Given an encrypted message, to decrypt.
 
 ## About the solution presented
 
<div align="justify"> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The program starts with reading p from the input and with 3 cases regarding p. The first case occurs when p is not prime and a corresponding message is displayed (“The number read is not prime”) and the program stops. When p is 2, it is displayed directly that the generator is 1, and when p is prime the search for the generator begins. 
<div align="justify">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To find the generator, each number (using $t1) is traversed to p-1 or until a generator is found and 2 vectors (a and v) are used, both of which retain the powers of the number (from $t1) modulo p. After all powers have been retained based on the formula g^k modulo p = g * g_previous_step modulo p, one of the vectors is sorted in ascending order to check the strict order relation. If the powers of the current number modulo p, represent all the elements from 1 to p-1, the generator has been found and displayed. If not, the program moves to the next number up to p-1. If no generator is found, the program displays a corresponding message and stops. 
<div align="justify">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Encryption and decryption require a memory-retained alphabet to be able to directly access the letters relative to it. For encryption, each letter of the given clear text was taken as input and the position of this letter in the alphabet was searched for; once the position was found (and retained in register $t2), the generator at position power (from $t2) modulo p was saved in another register, this power can be accessed using the unsorted vector (vector v), and the letter of the alphabet from the position of the second register specified above was displayed. For decryption, each letter of the given encrypted text was taken as input and the position of this letter in the alphabet was searched for; once the position has been found (and retained in the $t2 register), the power of the generator in the unsorted vector (vector v) is sought for which its value is equal to the position in the alphabet. The letter of the alphabet corresponding to the found power is displayed.
