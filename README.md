# Message Encryption
**Project developed in Assembly language, MIPS64 Architecture**

## About the project

The project meets the following requirements:
* <div align="justify"> For a number *p* it is desired to determine the generator (smallest) *g* so that this generator, successively raised to power, modulo *p*, generates all the elements from 1 to *p* - 1;
* Given a clear message, to encrypt.
* Given an encrypted message, to decrypt.
 
 ## About the solution presented
 
<div align="justify"> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The program starts with reading p from the input and with 3 cases regarding p. A case takes into account when p is not prime and a corresponding message is displayed (“The number read is not prime”) and the program stops . When p is 2, it is displayed directly that the generator is 1, and when p is prime the search for the generator begins. 
<div align="justify"> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;To find the generator, each number (using $ t1) is traversed to p-1 or until a generator is found and 2 vectors (a and v) are used, both of which retain the powers of the number (from $ t1) modulo p. After all powers have been retained based on the formula $g^k$ modulo p = g * g_previous_step modulo p, one of the vectors is sorted in ascending order to check the strict order relation. If the powers of the current number modulo p, represent all the elements from 1 to p-1, the generator has been found and displayed. If not, the program moves to the next number up to p-1. If no generator is found, the program displays a corresponding message and stops.
