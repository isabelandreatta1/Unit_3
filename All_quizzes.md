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

**Flowchart** 

![Flowchart2](https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Flowchart_Quiz_20.png)

### Quiz 21
Create a function that outputs a bracket emoji with both arms. The input given its face and its left arm. The right arm is a mirror image of the left arm. 

```py
#create class for oop 
class Solution:
    def __init__(self, input2, input1):
        # only attributes needed are the two inputs, both are strings 
        self.input2 : str = input2 #input2 is the lrft arm 
        self.input1 : str = input1 #input1 is the face 

    #create method to create the right arm of the emoji 
    def BracketEmoji(self):
        input2 = self.input2
        input1 = self.input1
        #create empty string for the right arm 
        newinput = ""
        #for loop which counts backwards since the right arm is the mirror image of the left arm
        #iterate through every charadcter in the left arm/input 2 
        for i in range(len(input2),0,-1):
            #convert the characters into ASCII code 
            #if the ascii number is either 91,123 or 60, the mirrored character is 2 numbers largers  
            if (ord(input2[i-1])) == 91 == 123 == 60:
                #add the characters to the right arm as a string 
                newinput += str(chr(ord(input2[i-1])+2))

            #if the ascii number is 92, then the mirrored character is 45 numbers less 
            elif (ord(input2[i-1])) ==92:
                newinput += str(chr(ord(input2[i-1])-45))

            #if the ascii number is 40, then the mirrored character is one more 
            elif ord(input2[i-1]) == 40:
                newinput += str(chr(ord(input2[i-1]+1)))

            #if the ascii number is 47, then the mirrored character is 45 more
            elif ord(input2[i-1]) == 47:
                newinput += str(chr(ord(input2[i-1])+45))

            #all other characters don't have a mirrored character so they can remain the same 
            else:
                newinput += str(input2[i-1])

        #return leftarm, face, rightarm 
        return input2 + input1 + newinput

print(Solution(input2 = "|-",input1 = "(~n~)").BracketEmoji())
print(Solution(input2 = "o-",input1 = "('|-|')").BracketEmoji())
print(Solution(input2 = "<...\ ", input1 = "[?????]").BracketEmoji())
``` 
**Testing**

![Testing5](https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Quiz21_testing.png)

### Quiz 22 

```py 
class Solution:
    #create class for solution
    def __init__(self, input):
        #attribute needed is input, it is a string
        self.input: str = input

    def BlackBoxProgram(self):
        input = self.input
        #split the iput by each word by seperating them by spaces
        newinput = input.split(" ")
        #create an empty list for the output
        output = ""
        #create for loop which will reiterate for every word in the list
        for word in newinput:
            #if the length of the word is less or equal to 2,
            if len(word) <= 2:
                #then that means that there is no spaces between and you can just output the word 
                output += word + " "
            #if the space between the first and the last letter is more than 0 (or the length of the word is more than 2) 
            else:
                #then you output the first letter, the length of the letter minus the first two letters, and the last letter 
                output += word[0] + str(len(word)-2) + word[-1] + " "

        return output

print(Solution("internationalization").BlackBoxProgram())
print(Solution("localization").BlackBoxProgram())
print(Solution("Hello world !").BlackBoxProgram())
print(Solution("98 99 100 101 102").BlackBoxProgram())
print(Solution("(codin) + (game) = (codingame)").BlackBoxProgram())
```

**Testing** 

![Testing6](https://github.com/isabelandreatta1/Unit_3/blob/main/folder/Quiz22_testing.png)

MarkScheme

1: Coded

2: Tested

3: Good coding practices
