### Big O Notation
<div>
1- Ignores constants
<div>2- Certain terms "dominate" others : O(1) < O(logn) < O(n) < O(nlogn) < O(n^2) < O(2^n) < O(n!)
<div>

![Alt text](bigO.png)

## Constant Time
O(1) -> Independente do  input ex : x = 5 + 15*20 resultará sempre no mesmo resultado n importa o N(input)
<div>O(n) -> Varia dependendo do input de n : 

```kotlin
fun test(n:Int){
for(i in 0..n){
  print i
}}
```
O(n^2) -> Dois loops por exemplo, qualquer funçao que seja n*n
```kotlin
fun test(n:Int){
for (i in 0..n)
for (j in 0..i)
print(j)
}
```