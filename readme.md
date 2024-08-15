## Hashpass-Rust: Hash-Based Password Generator

**Hashpass-Rust** is a command-line utility that generates secure passwords using a hashing algorithm. Here's how it works:

1. **Algorithm Overview**:
   - Prompt the user for the words "seed" and "key."
   - Use the Argon2 hashing function to generate a hash of 46 integers between 0 and 255 using the provided seed and key.
   - Transform the first 16 numbers into a character string called "res" using modulo indices.
   - Process the following 16 integers:
     - If the index is even, store the integer in the variable "pos."
     - Replace the character at index "pos" in "res" with an indexed lowercase character if the index is odd.
     - Repeat steps 4 and 5 for uppercase, numeric, and special characters.
     - Reduce the number of integers taken in each loop by half.
     - This ensures that the end result contains at least one of each character type.
   - Copy the final "res" string to the system clipboard and print it.

2. **About the Project**:
   - No detailed description, website, or specific topics are provided in the repository.
   - The project is written in Rust (93.8%) and Nix (6.2%).
   - You can find the code and contribute to the project on [GitHub](https://github.com/Konseptt/Hashpass-Rust).

Feel free to explore the code and experiment with the password generation process! If you have any further questions or need additional details, let me know. 😊

![GitHub Repository](https://github.com/Konseptt/Hashpass-Rust)

¹: [GitHub - Konseptt/Hashpass-Rust](https://github.com/Konseptt/Hashpass-Rust)
