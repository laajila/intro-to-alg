# intro-to-alg
## chapter 0 
- let f(n) and g(n) be functions f=O(g) if there is c>0 and n0 where f(n) <= c * g(n) for n>n0
- we can use limits to prove this, if lim f/n <infinity then f=O(g) if lim f/n < C and c >0 then f=Tot(g)
- if f = omega(g) then g = O(f)
- if f=omega(g) and f=O(g) it means f=Tot(g)

- to simplify functions :
  - multiplicative constants can be omitted 14n becomes n
  - n^a dominates n^b if a > b (n^2 dominates n)
  - any exponential dominates any polynomial : 3^n dominates n^5 (it also dominates 2^n)
  - any polynomial dominates any logarithm : n dominates log(n)^3 and n^2 dominates nlog(n)

## chapter 1 

- 2 ^Log(N) = N 
- Log(N) is the number of times you half N to get 1.
- i'ts the number of bits in the binary representation of N (ceil of log(N+1)) => b is the base with k digits in base we can express N=b^k-1, you can see this with 999=10^3-1. so k the number of bits logb(N+1)
- the depth of a complete binary tree with N nod. is log N . this comes from the fact that a perfect binary tree has 1 node at level ,  2 nodes at level 2, 2^2 at level 3, 2^h at level h if we do the addition to get total number of nodes: 1 + 2 + 2^2 + ...+ 2^h-1 + 2^h = 2^(h+1) - 1 / (2-1)=2^h+1 -1. if we think of a binary tree that just has one node in level h , the sum is different 1 + ...+ 2^h-1 + 1 (node over level h-1)=2^h. in conclusion 2^h<=N<2^h+1 so h<=logN < h+1 => h=floor(Log(N)).
- 1+1/2+1/3+ ... + 1/N = log(N)
- euclid algorithm : if x and y are positive integers with x>=y then gcd(x,y) =gcd(xMody , y)
- if a>=b then a mod b < a/2
- if d divides a and b and d=ax+ay <=> d=gcd(a,b)
- for any mod N , a has a multiplicative inverse modulo N if and only if it is relatively prime to N meaning gcd(a,N) = 1 (I don't understand this)
- fermat's little theorem : if p is prime then for every 1<= a < p a^(p-1)=1 mod(p)
- if a ^ N-1 =/= 1 mod(N) for some a relatively prime to N , then it must hold for at least half the choices of a < N : what this means is that of fermat test fails for one number it will fail for half the numbers < N. which means fermat is reliable to test primality except for CarMichael number.
- If N is prime, then a ^ N−1 ≡ 1 mod N for all a < N. => this means algorithm return yes if N is prime =1 
- If N is not prime, then a ^ N−1 ≡ 1 mod N for at most half the values of a < N. => probability of the algorithm wrongly returning yes <= 1/2 , if we repeat the operation k time it's 2^-k probability which is at 100 very low.
- Lagrange's prime number theorem let Pi(x) the number of primes <= x then Pi(x) ~ x/ln(x)

I am at 1.4