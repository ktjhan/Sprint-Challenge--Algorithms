#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) 0(n), numbers is ran once and doesn't see to change its behavior


b) 0(n^2), there's a loop nested inside an outer loop


c) 0(n), recursion is being called here

## Exercise II

First, let's understand the question we're trying to solve...

I believe it will have 2 parameters(floor,eggs)

Egg gets broken if it is thrown off floor f or higher, and doesn't get broken if dropped off a floor less than floor f. 

My educated guess will be that binary search is used, to be effective with this problem. We don’t know what floor exactly will start breaking the eggs, so it’ll be a guess and trial error, which would make the time linger. By splitting them up into two, we can work our way faster than linear search.

pseudocode would go along like this:
    divide up the building floor total by 2
    work our way to the left side, looping throgh the bottom floors and seeing if the egg(s) break
    if that doesn't work, then move on to the higher floors, and see if the egg(s) break through looping
    if you found the floor that breaks the egg(s), return the floor, and assume also that higher floors are included

runtime to my knowledge would be 0(n), we don't know how many floors? If we do know the number of floors, then 0(logn)