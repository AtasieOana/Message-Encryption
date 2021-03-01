# Message Encryption
**Project developed in Assembly language, MIPS64 Architecture**

## About the project

The project meets the following requirements:
<div align="justify"> * For a number *p* it is desired to determine the generator (smallest) *g* so that this generator, successively raised to power, modulo *p*, generates all the elements from 1 to *p* - 1;
* Given a clear message, to encrypt.
* Given an encrypted message, to decrypt.
 
 ## About the solution presented
 
<div align="justify"> The program starts with reading p from the input and with 3 cases regarding p. A case takes into account when p is not prime and a corresponding message is displayed (“The number read is not prime”) and the program stops . When p is 2, it is displayed directly that the generator is 1, and when p is prime the search for the generator begins.
