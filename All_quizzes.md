### Quiz 13
Given an array of food items and price, calculate the total price based on the table of tax categories below:

### Quiz 17 
Given three ints, a b c, one of them is small, one is medium and one is large. Return true if the three values are evenly spaced, so the difference between small and medium is the same as the difference between medium and large

``` py
def evenlySpace(a,b,c):
    #if b is the middle number
    if a>b and b>c:
        #then return if the difference between the middle number and larger/smaller number are equal
        return(abs(a-b) == abs(b-c))

    elif b>a and a>c:
        #the same as above but here the a is the middle number
        return(abs(b-a) == abs(a-c))
    else:
        #If the middle number is not a nor b, then it must be c
        return(abs(c-b)==abs(b-a))

print(evenlySpace(2,4,6))
print(evenlySpace(4,6,2))
print(evenlySpace(4,6,3))

``` 

**Testing:**


### Quiz 18 
Given a number as a String N. Multiply all the digits of N, and repeat the same with the product obtained till the product consists of only one digit. Output the number of steps taken to do so.

### Quiz 19 
Reverse Mode: Given the input/outputs shown, create the program that produces the output. Binary to decimal


### Quiz 20 
For each pair of characters of an input String, swap the two characters.


MarkScheme

1: Coded

2: Tested

3: Good coding practices
