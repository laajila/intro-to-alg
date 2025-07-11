# intro-to-alg
## chapter 0 
- let f(n) and g(n) be functions f=O(g) if there is c>0 where f(n) <= c * g(n)
- if f = omega(g) then g = O(f)
- if f=omega(g) and f=O(g) it means f=Tot(g)

- to simplify functions :
  - multiplicative constants can be omitted 14n becomes n
  - n^a dominates n^b if a > b (n^2 dominates n)
  - any exponential dominates any polynomial : 3^n dominates n^5 (it also dominates 2^n)
  - any polynomial dominates any logarithm : n dominates log(n)^3 and n^2 dominates nlog(n)

### Exercises
#### 01
a) n - 100/ n -200 <= 1/2 and  n - 200 / n - 100 <= 200 ==> SO it's f=Tot(g)
b) f/g=(n^1/2)/(n^3/2)=n^-1=1/n <= 1 and  g/f=n ==> So f=O(g)
c) f/g <=100 and g/f <=1/100 ==> SO f=Tot(g)
d) f/g <=1/10 and g/f>=10
e) f/g <=log(2)/log(3) and g/f <= log(3)/log(2) ==> f=tot(g)
f) f/g<=5 and g/f<=1/5  ==> f=tot(g)
g) f/g = n^0.01/log(n)^2  