# Folder-Encrypter

Projects aims at building a folder locker to maintain the confidentiality and integrity of data present inside the folder in the form of text files and encrypt and decrypt confidential files using RSA Algorithm. This software to act like a shield and protect system files and folders And because locking your folders makes them inaccessible, they cannot be deleted, damaged, or harmed in any other way.

## Languages and Softwares Used

1. C Programming Language - General-purpose, procedural computer programming language supporting structured programming and lexical variable scope.
2. Microsoft Visual Studio - Integrated development environment from Microsoft. Visual Studio dev tools & services make development easy for C++ language.
3. GCC(Gnu C Compiler) - Optimizing compiler produced by the GNU Project supporting various programming languages, hardware architectures and operating systems.

## Methodology

### RSA (Rivest,Shamir, Adelman) Cryptographic Algorithm:

RSA algorithm is asymmetric cryptography algorithm. Asymmetric actually means that it works on two different keys i.e. Public Key and Private Key. As the name describes that the Public Key is given to everyone and Private key is kept private. The idea of RSA is based on the fact that it is difficult to factorize a large integer. The public key consists of two numbers where one number is multiplication of two large prime numbers. And private key is also derived from the same two prime numbers. So if somebody can factorize the large number, the private key is compromised. Therefore encryption strength totally lies on the key size and if we double or triple the key size, the strength of encryption increases exponentially.

Following calculations are necessary for implementing RSA Algorithm:-

a) For generating Public Key -

For this we will select two prime numbers, P and Q. The first part of the public key will be calculated as : n=P*Q. For instance, let us assume P=53 and Q=59. Hence n = 53*59=3127

A small exponent e is also required. The constrainst for choosing e is as follows:-

1. It should be an integer 
2. It shouldn’t be a factor of n 
3. 1<e<function of (n)

b) For generating Private key-

Now we need to calculate function(n): Such that function(n)= (P-1)(Q-1)

so, function(n)=3016

Calculating Private key, d: d=(k*function(n) +1) / e for some integer k for k =2, value of d is 2011.

We will encrypt the text by first converting all the to their Ascii values and then we will apply the following formula, f^e mod n, where f is the ascii value of the alphabet to be encrypted. To decrypt the encrypted alphabet, we will use the following formula, c^d mod n, where c is the encrypted alphabet. Our motive to use cipher algorithms is to generate stronger passwords. We can create our own unique cipher algorithms. For example we can first apply a monoalphabetic cipher to our text before using RSA. This generates a higher level of password entropy.

For a more detailed explanation of this project check [*Folder_Encrypter_Document.pdf*](https://github.com/AnshumanSrivastava108/Folder-Encrypter/blob/main/Folder_Encrypter_Document.pdf) and [*Folder_Encrypter_presensation.pptx*](https://github.com/AnshumanSrivastava108/Folder-Encrypter/blob/main/Folder_Encrypter_presensation.pptx)

### Folder Locking

In computing, cacls and its replacement, icacls, are Microsoft Windows native command line utilities capable of displaying and modifying the security descriptors on folders and files. An access control list is a list of permissions for securable object, such as a file or folder, that controls who can access it.

To lock your file or folder type cacls "File Path" [/t] /e /p everyone:n. The /t is used to lock all folders and files within a folder. My file is located at C:\Users\Michael\Desktop\Cool\testdoc.txt, so I will type cacls "C:\Users\Michael\Desktop\Cool\testdoc.txt" /e /p everyone:n.

har mych2[]="\" /t /e /p everyone:n"; -To lock the folder

har mych2[]="\" /t /e /p everyone:f";-To Unlock the folder

## Results

Recognizing Human:

<p align="center">
<img width="600" height="350" src="Images/1.jpg ">
</p>

RSA Alogorithm Implementation:

<p align="center">
<img width="600" height="350" src="Images/2.jpg ">
</p>

Encryting the File:

<p align="center">
<img width="600" height="350" src="Images/3.jpg ">
</p>

Folder Protection: 

<p align="center">
<img src="Images/4.jpg ">
</p>

## References

1. https://ieeexplore.ieee.org/abstract/document/6021216
2. https://www.instructables.com/id/How-to-Lock-a-Folder-in-Windows-Using-Cmd/
3. https://scialert.net/fulltextmobile/?doi=itj.2013.1818.1824
4. Shireen Nisha, Mohammed Farik , RSA Public Key Cryptography Algorithm – AReview , 07, JULY 2017
5. Aized Amin Soofi,Irfan Riaz, Umair Rasheed, An Enhanced Vigenere CipherForData Security, 03, MARCH 2016
6. Rajeev Sobti, G.Geetha, Cryptographic Hash Functions: A Review, March 2012
7. Tonni Limbong, Testing the Classic Caesar Cipher Cryptography using ofMatlab, 0 2, February-2017 .
8. https://en.m.wikipedia.org/wiki/Cacls

## Author

**Anshuman Srivastava**

* Twitter: [@Anshuman_121](https://twitter.com/Anshuman_121)
* Github: [@AnshumanSrivastava108](https://github.com/AnshumanSrivastava108)
* LinkedIn: [@AnshumanSrivastava108](https://www.linkedin.com/in/anshumansrivastava108)





