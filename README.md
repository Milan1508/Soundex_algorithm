# Soundex_algorithm

#### Phonetic hashing is done using the Soundex algorithm. American Soundex is the most popular Soundex algorithm. It buckets British and American spellings of a word to a common code. It doesn’t matter from which language the input word comes; if the words sound similar, they will get the same hash code.


Let’s arrive at the Soundex of the word ‘Mississippi’. To calculate the hash code, you’ll make changes to the same word, in-place, as follows:

 * Phonetic hashing is a four-letter code. The first letter of the code is the first letter of the input word and is hence retained as it is. The first character of the phonetic hash is ‘M’. Now, you need to change the rest of the word’s letters.
 * Now, you must map all the consonant letters (except the first letter). All the vowels are written as they are, and the ‘H’s, ‘Y’s and ‘W’s remain unencoded (i.e., they are removed from the word). After mapping the consonants, the code becomes MI22I22I11I.


 * The third step is to remove all the vowels. In this code, ‘I’ is the only vowel. After removing all the ‘I’s, you get the code M222211. You must merge all the consecutive duplicate numbers into a single unique number. All the ‘2’s’ are merged into a single ‘2’, and all the ‘1’s’ are merged into a single ‘1’. The code that you get is M21.

 * The fourth step is to force the code to make a four-letter code. It would help if you padded it with zeroes in case it is less than four characters in length if you truncated it from the right side in case it is more than four characters in length. Here, since the code’s length is less than four characters, you can pad it with one ‘0’ at the end. Therefore, the final code is M210.
