# Binary Tree 
Funciona com listas ordenadas ou entao com arvores binarias com raiz<div>
Complexidade O(logN)
<div>

[![yt](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=VmKkAQtnjsM&ab_channel=Programa%C3%A7%C3%A3oDin%C3%A2mica) <div>
![bst](https://upload.wikimedia.org/wikipedia/commons/thumb/d/da/Binary_search_tree.svg/1200px-Binary_search_tree.svg.png)

### Trabalha com nós, pais e filhos


```kotlin
class Node<E>(val value: E, var left: Node<E>? = null, var right: Node<E>? = null)

fun higher(root: Node<Int>?, k: Int): Int? {
    if (root == null) {
        return null
    }

    var current: Node<Int>? = root
    var result: Int? = null

    while (current != null) {
        if (current.value <= k) {
            // Se o valor atual é menor ou igual a k, atualizamos o resultado
            // e continuamos procurando valores maiores na subárvore direita
            result = current.value
            current = current.right
        } else {
            // Se o valor atual é maior que k, descartamos a subárvore direita
            // e procuramos na subárvore esquerda
            current = current.left
        }
    }

    return result
}
```
