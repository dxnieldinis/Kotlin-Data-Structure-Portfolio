## Sliding Window 
Usado para percorrer arrays de modo eficiente.Obter substrings com metodo Janela deslizante<div>
[![Mail](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=GcW4mgmgSbw&t=413s&ab_channel=BytebyByte) QUICK EXPLANATION

[![Mail](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=MK-NZ4hN7rs&ab_channel=RyanSchachte) LONGER EXPLANATION
<div>

## Explicação rápida do que é 
Andar com uma janela em subsets de um array, deixando para tras os valores que estão fora da janela, otimizando o programa porque nao analisamos tudo de uma vez só. Armazena o melhor valor em variavel e vai mudando consoante percorremos, com o slide.


## Como identificar problemas com sliding window
Quando pedem a melhor soma de k elementos seguidos
valor minimo,maior,menor (talvez precisemos de calcular algo continuamente)


## Implementação 
```kotlin
fun maxsubArray(arr:IntArray,k:Int):Int{
    var bestsum=0
    var currentsum=0
    var left =0 
    var right=k-1
    while(right != arr.size){
        currentsum = arr[left] + arr[right] 
        
        if(currentsum>bestsum)bestsum= currentsum else
        bestsum=bestsum
        left++
        right++
        
        
    }
    return bestsum
    
} 
```