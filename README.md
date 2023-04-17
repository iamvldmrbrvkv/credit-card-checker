# credit-card-checker
Codeacademy's JavaScript project.

Project Goals
Context: You’re part of a research team that has found a new mysterious organism at the bottom of the ocean near hydrothermal vents. Your team names the organism, Pila aequor (P. aequor), and finds that it is only comprised of 15 DNA bases. The small DNA samples and frequency at which it mutates due to the hydrothermal vents make P. aequor an interesting specimen to study. However, P. aequor cannot survive above sea level and locating P. aequor in the deep sea is difficult and expensive. Your job is to create objects that simulate the DNA of P. aequor for your research team to study.

As you progress through the steps, use the terminal and console.log() statements to check the output of your loops and functions.

Project Requirements
1. Look over the starter code. There are 15 arrays that each contain the digits of separate credit card numbers. They all have prefixes to reflect their status, i.e. variables that start with valid contain a valid number, whereas invalid do not, and mystery variables can be either. There is also a batch array that stores all of the provided credit cards in a single array.

You’ll use these arrays later to check if your functions are working properly.

2. Create a function, validateCred() that has a parameter of an array. The purpose of validateCred() is to return true when an array contains digits of a valid credit card number and false when it is invalid. This function should NOT mutate the values of the original array.

To find out if a credit card number is valid or not, use the Luhn algorithm. Generally speaking, an algorithm is a series of steps that solve a problem — the [Luhn algorithm](https://en.wikipedia.org/wiki/Luhn_algorithm#Description) is a series of mathematical calculations used to validate certain identification numbers, e.g. credit card numbers. The calculations in the Luhn algorithm can be broken down as the following steps:

Starting from the farthest digit to the right, AKA the check digit, iterate to the left.
As you iterate to the left, every other digit is doubled (the check digit is not doubled). If the number is greater than 9 after doubling, subtract 9 from its value.
Sum up all the digits in the credit card number.
If the sum modulo 10 is 0 (if the sum divided by 10 has a remainder of 0) then the number is valid, otherwise, it’s invalid.
Here’s a [visual that outlines the steps](https://content.codecademy.com/PRO/independent-practice-projects/credit-card-checker/diagrams/cc%20validator%20diagram%201.svg?_gl=1*1q7kwrr*_ga*NDk3Mzk5MDMyMy4xNjc3Njk2MDE3*_ga_3LRZM6TM9L*MTY4MTczMjY4My4xNzguMS4xNjgxNzMzNTY2LjYwLjAuMA..). Check your function using both the provided valid and invalid numbers.

3. 
Create another function, findInvalidCards() that has one parameter for a nested array of credit card numbers. The role of findInvalidCards() is to check through the nested array for which numbers are invalid, and return another nested array of invalid cards.

4. After finding all the invalid credit card numbers, it’s also necessary to identify the credit card companies that have possibly issued these faulty numbers. Create a function, idInvalidCardCompanies() that has one parameter for a nested array of invalid numbers and returns an array of companies.

Currently, there are 4 accepted companies which each have unique first digits. The following table shows which digit is unique to which company:

First Digit	Company
3	Amex (American Express)
4	Visa
5	Mastercard
6	Discover
If the number doesn’t start with any of the numbers listed, print out a message like: “Company not found”.

idInvalidCardCompanies() should return an array of companies that have mailed out cards with invalid numbers. This array should NOT contain duplicates, i.e. even if there are two invalid Visa cards, "Visa" should only appear once in the array.

Project Extensions & Solution

5. Great work! Visit [our forums](https://discuss.codecademy.com/t/credit-card-checker-challenge-project-javascript/462375?_gl=1*ews761*_ga*NDk3Mzk5MDMyMy4xNjc3Njk2MDE3*_ga_3LRZM6TM9L*MTY4MTczMjY4My4xNzguMS4xNjgxNzMzNTY2LjYwLjAuMA..) to compare your project to our sample solution code. You can also learn how to host your own solution on GitHub so you can share it with other learners! Your solution might look different from ours, and that’s okay! There are multiple ways to solve these projects, and you’ll learn more by seeing others’ code.

6. If you’d like to challenge yourself further, you could consider the following:

Use different [credit card numbers from a credit card number generator and validator site](https://www.freeformatter.com/credit-card-number-generator-validator.html) and test if your functions work for all types of credit cards.
To make it easier to test credit card numbers, create a function that accepts a string and converts it into an array of numbers like the initially provided arrays. (Check the hint for a helpful function)
Create a function that will convert invalid numbers into valid numbers.