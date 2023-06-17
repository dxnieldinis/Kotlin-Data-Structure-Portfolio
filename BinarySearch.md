### Binary Search
Temos um array ordenado, e queremos encontrar um element dentro desse mesmo array, entao dividimos o problema ao meio e andamos para a esquerda ou para a direita a procura do elemento de forma mais eficiente 


```kotlin
fun binarySearch(arr: IntArray, element: Int): Int {
    var left = 0
    var right = arr.size - 1

    while (left <= right) {
        val mid = left + (right - left) / 2

        if (arr[mid] == element) {
            return mid  // Element found at index 'mid'
        } else if (element < arr[mid]) {
            right = mid - 1  // Element is in the left half
        } else {
            left = mid + 1   // Element is in the right half
        }
    }

    return -1  // Element not found in the array
}
```

Inicialmente, você precisa ter um array ordenado em ordem crescente.<div>
A busca binária começa definindo dois índices: o índice inicial (esquerda) e o índice final (direita) do array.<div>
Enquanto o índice inicial não ultrapassar o índice final:<div>
Calcule o índice médio, que é a média entre o índice inicial e o índice final. Isso é feito dividindo a soma dos índices por 2.<div>
Compare o elemento do índice médio com o elemento que você está procurando.
Se o elemento do índice médio for igual ao elemento procurado, você encontrou o elemento e pode retornar o índice médio.<div>
Se o elemento do índice médio for menor do que o elemento procurado, ajuste o índice inicial para o índice médio + 1 e continue a busca na metade direita do array.<div>
Se o elemento do índice médio for maior do que o elemento procurado, ajuste o índice final para o índice médio - 1 e continue a busca na metade esquerda do array.<div>
Se o elemento não for encontrado após o término do loop, significa que o elemento não está presente no array e você pode retornar um valor indicando que o elemento não foi encontrado.
