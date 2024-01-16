# hashcode

> Hash-based password generator for command-line use

## The Algorithm

1. Prompt for the words'seed' and 'key'
2. Using Argon2, generate a hash of 46 integers between 0 and 255 using the'seed' and 'key' functions.
3. Using modulo indices, transform the first 16 numbers to the character string'res'.
4. Using the following 16 integers:
   1. If the index is _even_, put the integer in the variable 'pos'.
   2. Replace index 'pos' of'res' with an indexed LOWERCASE character if the index is _odd_.
5. Repeat steps 4 through 5 for UPPERCASE, NUMERIC, and SPECIAL characters.
   Reduce the amount of integers taken in each loop by half.
   It can be shown that this results in at least one of each sort of character in the end result.
6. Copy'res' to the system clipboard and print it.

## Argon2 configuration

'Argon2id' is a variant.
'13' is the version number.
Memory price: '65536'
'4' iterations
'8' parallelism factor
'8' is the length of the hash.
