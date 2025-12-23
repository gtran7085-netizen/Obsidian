## If height is given 
mid nodes n = h + 1
max nodes  = $2^{h+1}$ - 1
## If nodes is given 
max height h = n - 1
min height h = $\log_2 (n + 1)$ - 1
## Strict tree
Mỗi node **hoặc có đúng 2 con, hoặc không có con nào**
## n-ary tree

## Strict m-ary tree
### If height is given
min nodes n = m*h  + 1
max nodes n = $m^{h+1}$ - 1 / m -1
### If nodes is given
min height h = $log_m[{n*(m-1) +1}]$ - 1
max height h = n - 1 / m
e =(m -1)* *i  + 1
## Representation of Binary tree
### Array
element = i
L.child = 2*i
R.child = 2*i  +1
Parent = floor(i / 2)
## Linked 
n + 1 = nullptr 

