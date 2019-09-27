Goal of the below test:

This is a simple (very last minute) Ruby based coding test that I think is fair for a relatively inexperienced Ruby engineer.

Justifications for this format:

1: Show that the applicant can understand a very (very) simple algorithm.

2: Demonstrate an understanding of web technologies, and the ability to set up a simple server with different end points.

3: Demonstrate a good approach to OO practices (I would expect a decent applicant to have the encoding and decoding logic outside of the endpoint logic.

4: Demonstrate knowledge of end to end tests. I'd expect to see unit tests surrounding the encoding and decoding logic, that demonstrate an understanding of edge cases and the ability to try to break your own code.

5: Demonstrate logic of end to end testing via posting to the end points with RSpec (or something similar).

6: Demonstrate the ability to clearly write commit messages as the application comes together.

7: Demonstrate the ability to to document API end points - if not technically, at least explain how to use them.

I know that these skills are all taught on Makers Academy, so I'd expect any competent junior Ruby engineer to be able to implement this to a relatively good standard.

Please feel free to leave comments / suggestions / improvements, though this does need to go out by the end of the day!




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
