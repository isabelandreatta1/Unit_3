### Quiz 13
Given an array of food items and price, calculate the total price based on the table of tax categories below:
```py
#List of all items in grocery store and their respective categories
Food = ["bread", "smoked salmon", "apples", "cambert Cheese"]
Electronics = ["ipad", "huawei P30", "toshiba TV"]
Liquer = ["beer", "whiskey", "sake"]

def Totalprice(item,rate):
    totalprice = 0
    #Above is total price counter
    for i in range(len(item)):
        #for loop which iterates through every item in the input
        if item[i] in Food:
            #if the item is in the food list, then the total price will be the rate of the item
            # with a tax of 10%
            totalprice += rate[i] * 1.1
        if item[i] in Electronics:
            #if the item is in the electronics list, the tax will be 15%
            totalprice += rate[i] * 1.15
        if item[i] in Liquer:
            #if the item is in the liquer list, the tax will be 20% 
            totalprice += rate[i] * 1.2
        else:
            #if the input is not written in any of the lists
            #then print error 
            print("Error")

    return(totalprice)

print(Totalprice(item = ["bread","beer","ipad"],rate = [300,800,30000]))
print(Totalprice(item = ["smoked salmon","apples","sake"],rate = [1200,400,4000]))
print(Totalprice(item = ["toshiba TV", "whiskey", "cambert Cheese"],rate =[10200,2000,799]))
``` 
**Flowchart** 
![Flowchart](https://github.com/isabelandreatta1/Unit_3/blob/main/folder/FlowChart_Chapter13.png)

### Quiz 17 
Given three ints, a b c, one of them is small, one is medium and one is large. Return true if the three values are evenly spaced, so the difference between small and medium is the same as the difference between medium and large

``` py
class Solutions:
    def __init__(self,a,b,c):
        self.a: int = a
        self.b: int = b
        self.c: int = c

    def evenlySpace(self):
        a,b,c = self.a, self.b, self.c
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

print(Solutions(2,4,6).evenlySpace())
``` 

**Testing:**
![Testing1](https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Quiz17_testing.png)


### Quiz 18 
Given a number as a String N. Multiply all the digits of N, and repeat the same with the product obtained till the product consists of only one digit. Output the number of steps taken to do so.
``` py 
class Solution:
    #create class 
    def __init__(self,N):
        self.N: str = N
        #only attribute needed is N, or the input 

    def onlySingleDigit(self):
        N = self.N
        step = 0
        #this will be the counter for the number of steps 
        while len(N) > 1:
            #length of N is equal to number of digits 
            #while number of digits is above 1 ... 
            product = 1
            for i in range(len(N)):
                product *= int(N[i])
                #multiply it for every digit 
                #this for loop iterates through each index 

            N = str(product)
            #convert product into string again 
            step += 1
            #add one step 

        return step
    
print(Solution("39").onlySingleDigit())


``` 


**Testing:**
![Testing2](https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Quiz18_testing.png)

### Quiz 19 
Reverse Mode: Given the input/outputs shown, create the program that produces the output. Binary to decimal
```py
class Solution:
    #initaliser, only attribute needed is input
    def __init__(self,input):
        self.input: str = input

    #create method
    def ReverseMode(self):
        input = self.input
        #split the string by every exclamation mark
        newList = input.split("!")
        #create for loop to iterate through every item/binary number
        for i in range (len(newList)):
            #method which converts binary to decimal
            print(str(int(newList[i], 2)), end="")
        return


Solution(input ="100!000!111").ReverseMode()
``` 


**Testing:**

![Testing3](https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Quiz19_testing.png)


### Quiz 20 
For each pair of characters of an input String, swap the two characters.
```py
class Solution:
    def __init__ (self,input):
        #only attribute needed is the input
        #input is a string
        self.input : str = input

    def replaceStringByTwo(self):
        input = self.input
        newstring = ""
        #create new empty string so we can add to this later
        if len(input)<2:
            #if the string is less than two characters
            return input
            # then return the input
        else:
            for i in range(0,len(input),2):
                #for every two letters in the string
                newstring += input[i+1] + input[i]
                #switch the order, by putting the second character first and the first character second
            return newstring

print(Solution("01ABxy").replaceStringByTwo())
print(Solution("k513bbcd").replaceStringByTwo())
print(Solution("F").replaceStringByTwo())
print(Solution("ErrorsShould").replaceStringByTwo())
``` 

**Testing:**
![Teting4](https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Quiz20_testing.png)


MarkScheme

1: Coded

2: Tested

3: Good coding practices
