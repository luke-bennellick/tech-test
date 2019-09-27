# Run Length Encoding web API

This problem is based around the concept of Run Length Encoding, which a simple form of data compression.

An example of run length encoding is as follows:

Input:
BBBBKKIEEEPPPPP

Output:
4B2KI3E5P

For any recurring sequential characters, we simply replace the sequence with the number of repetitions, and the character which is repeated.
Using this method, we have reduced a 15 character string to 9 characters, and it can be easily restored. More information on run length encoding can be found here: https://en.wikipedia.org/wiki/Run-length_encoding.

## The task

For this task, we would like you to implement a simple web API in Ruby. You are free to use any libraries you see fit.

This API should meet the following requirements:

1: As a user, I should be able to post an unencoded string to the API and have it returned in encoded format via the RLE algorithm.
2: As a user, I should be able to post an encoded string to the API and have it returned in unencoded format.

A simple html or JSON response is fine, and as this is a backend task, no styling is required at all.

## What we are looking for

Though fairly simple in nature, this task has good scope for demonstrating and understanding of Object Oriented best practices and test driven design.

A few hints:

1: Think about your commits, clearly communicate your approach
2: instructions to use your API should be included in the README
3: Ensure your tests are well structured, and consider edge cases.

## Technologies

You're free to use any Ruby technologies you see fit. Rails, Rails API, Padrino or pure Ruby are all fine. We're not looking for perfection, so please don't spend too long on the solution. We're just looking for an understanding of best practices, and structured engineering.


## Further example cases

### Encoding endpoint:

Input: OOOOFFFFFFKBGGGEEEEEEE
Output: 4O6FKB3G7E

Input: PPPPPPKKKEEEEEEEEE
Output: 6P3K9E

Input: OKEHDJ
Output: OKEHDJ

### Decoding endpoint:

Input: 6F3RF
Output: FFFFFFRRRF

Input: KDJUIO
Output: KDJUIO

Input: 12P6L
Output: PPPPPPPPPPPPLLLLLL
