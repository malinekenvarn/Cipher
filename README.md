# Cipher

This is another task I did for my university course in Java in 2019. The objective was to write a program that uses the kama sutra encryption system to encrypt a message. 

<h3>Background</h3>
This encryption system is based on 2 keys. Each key is exactly half of the english alphabet, every character can be found on either one of the keys, and the order is random.  When a message is to be encrypted, one take each character, find that character in one of the keys and then take the character on the same place in the other key.

<h3>My solution</h3>
Because this task was for a beginners course, I wanted to use only arrays, loops, and If-statements  to make my functions.
<br>

<b>keyGen:</b> This function generates and return 2 encryption keys(13 characters each)
Every letter in the English alphabet can be found in one of the keys, every letter is used one time.  First I made an array with room for 26 characters (English alphabet) and then  I made an algorithm that fills the array randomly. Every alphabetical character appears exactly once, because the algorithm loops through the array every time to see if the character is already present. Then the array  is split into two char arrays, they are the encryption keys. The function return a two dimensional array containing the two encryption keys.

<b>encryptMessage:</b>  This method receive a string with the message, and the two dimensional array containing the 2 keys. It will then encrypt the message: for every character in the string, the function will find that character in one of the 2 keys. Then it will find the character in same index of opposing key. If encryptMessage[i] is empty it means that there is a blank space , then it will be given ASCII value 32. A char array with encrypted message will be made in this way, and returned as a string.

<b>decryptMessage:</b> This function is basicly the same as encryptMessage. It takes the encrypted message and the keys and gives back the original message.

