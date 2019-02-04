#a3_cryptography
Cryptography ( Due 08 Feb 2019 )

Cryptography is an ancient study of secret writing. There is a wealth of literature in this field. An extremely readable book on this subject is The Code Book by Simon Singh. This is a field of study that is of particular relevance in Computer Science. Given the widespread use of computers, one of the things people are interested in is making transactions over the internet more secure.

Here is a simple and clever way to encrypt plain text. Assume that the message contains only lower case letters from a to z. Let L be the length of the original message, and M the smallest square number greater than or equal to L. Add (M-L) asterisks to the message, giving a padded message with length M. Use the padded message to fill a table of size K x K, where K2 = M. Fill the table in row-major order (left to right in each column, top to bottom for each row).

Now to encrypt, rotate the table 90° clockwise. The encrypted message comes from reading the message in row-major order from the rotated table, omitting any asterisks.

Let us say the original message is gonewiththewind. The message length L = 15 and so M = 16. The padded message is gonewiththewind*. Here are two tables showing the padded message and the padded message after rotation.

Original Padded Message
g	o	n	e
w	i	t	h
t	h	e	w
i	n	d	*

Rotated Padded Message
i	t	w	g
n	h	i	o
d	e	t	n
*	w	h	e

So the encrypted message (ignoring the asterisks) is itwgnhiodetnwhe.

The program that you will be writing will be called Cipher.py and must be modular. Here is the general outline of the program:

# takes a string and returns the encrypted string
def encrypt ( strng ):

# takes an encrypted string and returns the plain text version
def decrypt ( strng ):

def main():
  # open file encrypt.txt

  # encrypt and output all lines in file encrypt.txt

  # open file decrypt.txt

  # decrypt and output all lines in file decrypt.txt

main()
You can always add more functions than those listed.
Input: You will have two input files. The first file encrypt.txt will have the following format. The first line is the number N of original messages to encrypt, 1 ≤ N ≤ 100. The following N lines will each have a message to encrypt according the scheme given above. Each message contains only lower case characters a through z and each message will have a length between 1 ≤ L ≤ 100.

The second file decrypt.txt will have a similar format. The first line is the number N of encrypted messages to decrypt, where 1 ≤ N ≤ 100. The following N lines will each have a correctly encrypted message to decrypt. Each encrypted message will contain only lower case characters a through z and each encrypted message will have a length between 1 ≤ L ≤ 100.

The two input files are independent of each other. That is the number of lines of the first may not be the same as the second. There may not be a 1:1 correspondence between the lines of the two files.

Output: Your output will be on the console and will look something like this:

Encryption:
itwgnhiodetnwhe
osotvtnheitersec

Decryption:
gonewiththewind
thecontestisover
You must output Encryption: and Decryption: before each respective output, exactly as given in the sample output. Failure to do so will result in points being deducted.
For this assignment you may work with a partner. Both of you must read the paper on Pair Programming. . If you are working with a partner then both of you will submit the same code. In the header make sure that you have your name and your partner's name. If you are working alone then remove the fields that has the partner's name and EID.

The file that you will be uploading will be called Cipher.py. We are looking for clean and structured design. The file will have a header of the following form:

#  File: Cipher.py

#  Description:

#  Student Name:

#  Student UT EID:

#  Partner Name:

#  Partner UT EID:

#  Course Name: CS 313E

#  Unique Number:

#  Date Created:

#  Date Last Modified:

Use the Canvas system to submit your Cipher.py file. We should receive your work by 11 PM on Friday, 08 Feb 2019. There will be substantial penalties if you do not adhere to the guidelines. Remember Python is case sensitive. The name of your file must match exactly what we have specified.

Your Python program should have the proper header.
Your code must run before submission.
You should be submitting your file through the web based Canvas program. We will not accept files e-mailed to us.
Here is the Grading Criteria.
References

Simon Singh On Cryptography
History of Cryptography
An Overview of Cryptography
