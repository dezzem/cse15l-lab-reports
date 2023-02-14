# Grep Command Line Options 

`-v`

* Prints out all the lines *without* the pattern (Can be used with other options)

Examples:

`grep -v "" written_2/non-fiction/OUP/Castro/*.txt`

>Searches for text files without any spaces. Usefull for finding completely filled files.

![image](https://user-images.githubusercontent.com/122496316/218659697-947995f9-d450-4e97-8f21-fe6d30bfe8a3.png)

`grep -v "." written_2/non-fiction/OUP/Castro/*.txt` 

>Command searches for txt files without periods. Can help differenciate different types of documents.

![image](https://user-images.githubusercontent.com/122496316/218659826-a2b796a8-bf91-4c95-a978-aa16b28c3e25.png)

---
`-r`

* Allows grep to search recursively in all subdirectories

Examples:

`grep -r "hello" written_2/`

>Searches in all sub directories of written_2 for text files with the string hello. Helpful if you need to see how common a keyword is.

![image](https://user-images.githubusercontent.com/122496316/218657812-1c41794d-82d9-4c46-9318-a1611e2a9f70.png)

`grep -l -r "stormy" written_2/`

>Searches in all sub directories of written_2 for text files with the string stormy. Helpful if you're trying to find someplace stormy.

![image](https://user-images.githubusercontent.com/122496316/218658454-38ff28a7-2cb0-4966-8d51-939854e7bcd4.png)


---
`-i`

* Option makes the search case non-dependent on capitalization

Examples:

`grep -l -v "a" written_2/non-fiction/OUP/Abernathy/*.txt`

>Searches for all text files that don't use the letter a (Capitalized or not)

![image](https://user-images.githubusercontent.com/122496316/218659006-9103843f-82d9-4666-a551-ee0c8cf97d00.png)

`grep -l -v "the" written_2/non-fiction/OUP/Castro/*.txt`

>Searches for all text files that don't use the string the (Capitalized or not)

![image](https://user-images.githubusercontent.com/122496316/218659229-c5297ff8-b814-43f1-99af-1d5d22a2b28f.png)

---

`-l`

* Prints out only the names of the files that match rather than their content

Examples:

`grep -l "son" written_2/non-fiction/OUP/Abernathy/*.txt`

>Finds the names of all books that have the word son in them

![image](https://user-images.githubusercontent.com/122496316/218657296-57ad3839-1b0e-46ef-8485-051edbef6734.png)

`grep -l "father" written_2/non-fiction/OUP/Abernathy/*.txt`
>Finds the names of all books that have the word father in them

![image](https://user-images.githubusercontent.com/122496316/218657110-f6c7dd89-d176-420d-8c38-0b797f37a047.png)

### Source: https://www.digitalocean.com/community/tutorials/grep-command-in-linux-unix
