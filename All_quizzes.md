### Quiz 13
Given an array of food items and price, calculate the total price based on the table of tax categories below:
```py
Food = ["bread", "smoked salmon", "apples", "cambert Cheese"]
Electronics = ["ipad", "huawei P30", "toshiba TV"]
Liquer = ["beer", "whiskey", "sake"]

def Totalprice(item,rate): 
  totalprice = 0 
  for i in range(len(item)):
    if item[i] in Food: 
      totalprice += rate[i] * 1.1 
    if item[i] in Electronics: 
      totalprice += rate[i] * 1.15
    if item[i] in Liquer: 
      totalprice += rate[i] * 1.2

  return(totalprice)

print(Totalprice(item = ["bread","beer","ipad"],rate = [300,800,30000]))
print(Totalprice(item = ["smoked salmon","apples","sake"],rate = [1200,400,4000]))
print(Totalprice(item = ["toshiba TV", "whiskey", "cambert Cheese"],rate =[10200,2000,799]))
``` 


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


### Quiz 20 
For each pair of characters of an input String, swap the two characters.


**Testing:**


MarkScheme

1: Coded

2: Tested

3: Good coding practices
