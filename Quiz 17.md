Given three ints, a b c, one of them is small, one is medium and one is large. Return true if the three values are evenly spaced, so the difference between small and medium is the same as the difference between medium and large. 

```py 
def evenlySpace(a,b,c):
  if a>b and b>c:
    return(abs(a-b) == abs(b-c))

  elif b>a and a>c:
    return(abs(b-a) == abs(a-c))
  else:
    return(abs(c-b)==abs(b-a))

print(evenlySpace(2,4,6))
print(evenlySpace(4,6,2))
print(evenlySpace(4,6,3))
``` 

Result: 
True
True
False 
