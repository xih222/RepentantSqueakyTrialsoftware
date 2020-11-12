# CSE262 - Programming Languages - Homework 8

**Due Date: 11/09/2020 by EOD**

**This assignment is out of 8 points. All questions are weighted equally.**

## Instructions

1. Fork this repository into your CSE262 project namespace. [Instructions](https://docs.gitlab.com/ee/workflow/forking_workflow.html#creating-a-fork)
2. Clone your newly forked repository onto your development machine. [Instructions](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#clone-a-repository) 
3. As you are writing code you should commit patches along the way. *i.e.* don't just submit all your code in one big commit when you're all done. Commit your progress as you work. You should have at least one commit per question. **The assignment will not be accepted if you do not follow this procedure.**
4. When you've committed all of your work, there's nothing left to do to submit the assignment.

## Assignment

Solve the following 8 problems using the Haskell programming language. For each problem, commit a new file with the name as the question number. e.g. for Question one, commit a file with your solution as `question_1.hs`. Within each file you can define as many functions as you want, but the "main" function in the file (that will be called by the graders to check your work) should be named according to the question i.e. the first question function would be `question_1`

Each question is weighted equally. 1 point per question for a correct solution, partial points for an attempt that isn't correct.

*Note: If you want to write any formatted text in the Readme, make sure it is surrounded by a Markdown code fence to maintain the formatting in the rendered view (there are examples of how to do so in the source of this document). We will deduct 10% for poor formatting from here on out.*

For each problem I will ask you to write down the function signature in this Readme file. This is worth 20% of the points for each problem (i.e. since each problem is worth 1 point, writing down the function signature here is worth .2 points). surround the function signature in a code fence as in the following example:

```
question_0 :: (Num a) => a -> a -> [a]
```

**Also:** for each problem, you must write an explanation for how your solution works. A complete explanation will include a discussion of the design (e.g. why did you design it the way you did, what alternatives did you consider), a description of what the code does, and any shortcomings or sharp edges to your solution (e.g. are there any edge cases that are not handled, will the function fail on some input, is the implementation efficient, etc.). As part of your explanation, give an example of how the function is called, and what is the expected output. This is worth another 20% of points for each problem.

## Question 1

Given an unsorted array of numbers (you can assume they are of type `Int`), find all pairs with the given sum. For example, your function will have two inputs: 

1. An array of any length e.g. `[1, 8, 5, 2, 5, 6, 7, 3, 9, 4]`
2. A target sum e.g. `10`. 

The output will be an array of all pairs of numbers that sum to the target e.g. `[(1,9),(8,2),(5,5),(7,3),(6,4)]`. 

Before you go about implementing this function, write down the function signature here in the Readme:

```
question_1 :: Int a => [a] -> a -> [(a,b)]
```
```
Explanation: The function first sets the function signature, question_1, to accept an array input, then a sum input, and finally output an array list in terms of two. It would first set question_1 some value of x, and then it would set question_1 to take in another number of any length. It would then split the arrays into list of twos where each (a,b) would = the sum value.
```
## Question 2

Given an unsorted array of numbers (you can assume they are of type `Int`), find all numbers such that the number is greater than all elements that occur after it in the array. For example, given the array:

```
[10, 9, 1, 5, 7, 3, 6, 2]
```

Your function will return:

```
[10, 9, 7, 6]
```

Before you go about implementing this function, write down the function signature here in the Readme:

``` 
question_2 :: Int a => [a] -> a
```
```
Explanation: The function first sets the function signature, question_2, to accept an array input, and then output an array list. It would first set question_2 some value of x for array of any length, and then it would cut the array where for each item in the list, a number would be removed if less than the next value. 
```
## Question 3 

Given a string that represents the current time on a continuous 12 hour analog clock, calculate the smaller angle in degrees between the two hands.

For example given the string "9:00", the output will be 90.

Notice I've described the clock as operating continuously. That means after the hour, as the minute hand moves, the hour hand continues to move as well. So at 9:30, the hour hand will be half way between 9 and 10. Assume that the hour hand moves at a constant rate between numbers, so that at 10:00 it is pointing exactly to the 10, and at 10:01 it has moved 1/60th of the way to 11.

For example, given the input "2:30" the output will be 105.

Before you go about implementing this function, write down the function signature here in the Readme:

Explanation:

## Question 4

Given a M x N matrix, where each element is a number (you can assume they are of type `Int`), find the least cost path from the top left element to the bottom right element. Valid movements are only to adjacent elements (i.e. no diagonal movements). You can't visit an element more than once. For each path, calculate the sum of the elements in that path. The function should return the sequence corresponding to the lowest cost path. For example, let's say your input is a 2 x 3 matrix:

(this isn't Haskell code)

```
[6 9 3
 2 5 7]
```

The valid paths are:

```
6 -> 9 -> 3 -> 7 = 25
6 -> 9 -> 5 -> 7 = 27
6 -> 2 -> 5 -> 7 = 20
6 -> 2 -> 5 -> 9 -> 3 -> 7 = 32
```

The function will therefore return:

```
[6, 2, 5, 7]
```

Before you go about implementing this function, write down the function signature here in the Readme:

Explanation:

## Question 5

Write a function that multiplies two matrices together. If you're not familiar with matrix multiplication, you can read about that [here](https://en.wikipedia.org/wiki/Matrix_multiplication).

Don't use any built-in libraries or functions to do this. I want you to calculate the result at a granular level.

For example:

Let matrix A be:

```
[1 2 3
 4 5 6]
```

Let matrix B be:

```
[7 8
 9 10
 11 12]
```

Then A * B is:

```
1*7 + 2*9 + 3*11  = 58
1*8 + 2*10 + 3*12 = 64
4*7 + 5*9 + 6*11  = 139
4*8 + 5*10 + 6*12 = 154
A * B = [58  64
         139 154]
```

Notice that in order to do this calculation, we need the same number of rows in B as there are columns in A. If A were 2 x 4 and B were 3 x 2, we wouldn't be able to complete this computation. Your function should handle this, by returning the result of the matrix multiplication if it can be calculated, or something else if it can't.

Before you go about implementing this function, write down the function signature here in the Readme:

Explanation:

## Question 6

Given an array of numbers (you can assume they are of type `Int`), find the equilibrium index. The equilibrium index is the index of the array such that the sum of the numbers to the left of the equilibrium index is equal to the sum of the numbers to the right.

For example, given the following array:

```
[5 8 7 2 4 3 10 9 7]
```

The equilibrium index is 5, because `5 + 8 + 7 + 2 + 4 = 26` and `10 + 9 + 7 = 26`

It is possible that the given array does not contain an equilibrium index. Your function should handle this.

Before you go about implementing this function, write down the function signature here in the Readme:

Explanation:

## Question 7

Given an input string, remove all adjacent duplicate characters until no adjacent duplicates remain.

For example, given the string:

```
BZXYYXYYZA
```

The output will be `BA`.

This result will be found through multiple passes. In the first pass, duplicates will be removed to obtain `BZXXZA`

In the second pass the function will obtain `BZZA`

In the third and final pass the function will remove the final pair of duplicate letters to obtain `BA`

Before you go about implementing this function, write down the function signature here in the Readme:

Explanation:

## Question 8

Implement the [mergesort](https://en.wikipedia.org/wiki/Merge_sort) algorithm in Haskell. Your function should be able to accept characters and numbers.

Before you go about implementing this function, write down the function signature here in the Readme:

Since you can easily look this up on the internet (there are a billion implementations out there), and it's kind of difficult, I expect you'll probably glace at a solution. If you do, cite it here. That's fine. But for this problem the explanation of the code will be worth **60%** of the total points for this problem. We will be scrutinizing this one much more heavily, so give a good explanation. A cursory explanation will earn you very few points.

Explanation:
