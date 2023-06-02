# Regular Expression Exercises

## Exercise 1

Write a regular expression that matches the following:

1. Any word with `cat` in it
2. A line that starts with `cat`
3. A line that ends with `cat`
4. A line that has `cat` or `dog` in it


<details>
    <summary><strong>Exercise 1 Answers</strong></summary>

   1. Any word with `cat` in it
   > `.*cat.*`
   2. A line that starts with `cat`
   > `^cat.*`
   3. A line that ends with `cat`
   > `.*cat$`
   4. A line that has `cat` or `dog` in it
   > `.*(cat|dog).*`

</details>

<br/>

## Exercise 2 - Full Stop

Write a regular expression that matches the following:

1. Any string that starts with "hello" and ends with "world".
2. Any string that starts with a number and ends with a letter.
3. Any string that contains at least one digit and one letter, separated by a full stop.
4. Write a regular expression that matches any string that contains a valid IPv4 address in the format X.X.X.X, where X is a number between 0 and 255.

<details>
    <summary><strong>Exercise 2 Answers</strong></summary>

   1. Any string that starts with "hello" and ends with "world".
   > `^hello.*world$`
   2. Any string that starts with a number and ends with a letter.
   > `^[0-9].*[a-zA-Z]$`
   3. Any string that contains at least one digit and one letter, separated by a full stop.
   > `^[0-9]+[.][a-zA-Z]+$`
   4. Write a regular expression that matches any string that contains a valid IPv4 address in the format X.X.X.X, where X is a number between 0 and 255.
   > `^([0-9]|[1-9][0-9]|1[0-9][0-9]|2[0-4][0-9]|25[0-5])[.]([0-9]|[1-9][0-9]|1[0-9][0-9]|2[0-4][0-9]|25[0-5])[.]([0-9]|[1-9][0-9]|1[0-9][0-9]|2[0-4][0-9]|25[0-5])[.]([0-9]|[1-9][0-9]|1[0-9][0-9]|2[0-4][0-9]|25[0-5])$`

</details>

<br/>

## Exercise 3 - Ranges

Write a regular expression that matches the following:

1. Any word that is 5 characters long
2. Any word that is between 3 and 5 characters long
3. Any word that has a letter in it
4. A hexadecimal digit


<details>
    <summary><strong>Exercise 3 Answers</strong></summary>

   1. Any word that is 5 characters long
   > `\b^.{5}\b`
   2. Any word that is between 3 and 5 characters long
   > `\b.{3,5}\b`
   3. Any word that has a letter in it
   > `\b\w*[a-zA-Z]\w*\b`
   4. Any hexadecimal digit
   > `\b[0-9a-fA-F]+\b`

</details>

<br/>

## Exercise 4 - Quantifiers

Write a regular expression that matches the following:

1. A group of letters that are all uppercase and are between 3 and 5 characters long
2. A group of letters that are all lowercase and are between 3 and 5 characters long
3. A group of letters that are all uppercase or lowercase and are between 3 and 5 characters long

<details>
    <summary><strong>Exercise 4 Answers</strong></summary>

   1. A group of letters that are all uppercase and are between 3 and 5 characters long
   > `^[A-Z]{3,5}$`
   2. A group of letters that are all lowercase and are between 3 and 5 characters long
   > `^[a-z]{3,5}$`
   3. A group of letters that are all uppercase or lowercase and are between 3 and 5 characters long
   > `^[a-zA-Z]{3,5}$`

</details>

<br>

## Exercise 5 - Anchors

Write a regular expression that matches the following:

1. Any word that starts with "the"
2. Any word that ends with "ing"
3. A line that starts with a number and ends with a full stop
4. A line that contains the word "cat" but does not start with "cat"

<details>
    <summary><strong>Exercise 5 Answers</strong></summary>

   1. Any word that starts with "the"
   > ^the.*
   2. Any word that ends with "ing"
   > .*ing$
   3. A line that starts with a number and ends with a full stop
   > ^[0-9].*\.$
   4. A line that contains the word "cat" but does not start with "cat"
   > ^(?!cat).*cat.*$

</details>

<br/>

## Exercise 6 - Character Classes

Write a regular expression that matches the following:

1. Any word that starts with a vowel
2. Any word that starts with a consonant
3. A string that contains either "color" or "colour"
4. A line that starts with a lowercase letter and ends with a period

<details>
    <summary><strong>Exercise 6 Answers</strong></summary>

   1. Any word that starts with a vowel
   > ^[aeiouAEIOU].*$
   2. Any word that starts with a consonant
   > ^[^aeiouAEIOU].*$
   3. A string that contains either "color" or "colour"
   > .*colou?r.*
   4. A line that starts with a lowercase letter and ends with a period
   > ^[a-z].*\.$

</details>

<br/>

## Exercise 7 - Groups and Capturing

Write a regular expression that matches the following:

1. A string that starts with a word in all lowercase letters and ends with the same word in all uppercase letters (e.g., "helloHELLO")
2. A string that contains three consecutive identical characters (e.g., "aaabbbccc")
3. A string that contains a date in the format DD/MM/YYYY (e.g., "20/04/2023")
4. A line that contains the word "cat" immediately followed by the word "dog"

<details>
    <summary><strong>Exercise 7 Answers</strong></summary>

   1. A string that starts with a word in all lowercase letters and ends with the same word in all uppercase letters (e.g., "helloHELLO")
       > ^([a-z]+)([A-Z]+)$
   2. A string that contains three consecutive identical characters (e.g., "aaabbbccc")
       > ^.*(.)\1\1.*$
   3. A string that contains a date in the format DD/MM/YYYY (e.g., "20/04/2023")
       > ^(0[1-9]|[12][0-9]|3[01])\/(0[1-9]|1[0-2])\/\d{4}$
   4. A line that contains the word "cat" immediately followed by the word "dog"
       > .*cat(?=.*dog).*

</details>
