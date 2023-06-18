# MergeSort & QuickSort
### QuickSort 

Selecionando qualquer elemento, o objetivo é selecionar um pivo e deixar apenas elementos maiores a direita e menores a esquerda,depois recursivamente selecionar outro pivo etc etc.<div>



->  Eficiencia
 * Worst-case performance	    O(n^2)
 * Best-case performance	    O(nLogn)
 * Average performance      	O(nLogn)
 * Worst-case space complexity	O(1)
 
[![Mail](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=wx5juM9bbFo&list=PL5TJqBvpXQv4l7nH-08fMfyl7aDFNW_fC&index=6&ab_channel=Programa%C3%A7%C3%A3oDin%C3%A2mica) 

```kotlin
fun quicksort(list: IntArray, low: Int, high: Int) {
    if (low < high) {
        val pivot = partition(list, low, high)
        quicksort(list, low, pivot - 1)
        quicksort(list, pivot + 1, high)
    }
}

fun partition(list: IntArray, low: Int, high: Int): Int {
    val pivot = list[high]
    var left = low

    for (i in low until high) {
        if (list[i] <= pivot) {
            swap(list, i, left)
            left++
        }
    }

    swap(list, left, high)
    return left
}

fun swap(list: IntArray, i: Int, j: Int) {
    val temp = list[i]
    list[i] = list[j]
    list[j] = temp
}

```