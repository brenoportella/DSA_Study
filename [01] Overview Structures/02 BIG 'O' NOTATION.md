BIG O Notation serve para compreender tanto a complexidade temporal quanto a complexidade espacial de um algoritmo.
#### Complexidade Temporal

Dado o input de um algoritmo, tipo um array, o *big O* vai dizer quanto tempo vai levar para executar uma vez proporcionalmente ao tamanho do input.

Percorrer 1 vez. Complexidade de tempo seria **O(n)**.
Ou seja, o tamanho da complexidade, o tempo necessário, depende do quão grande é o array.

#### Complexidade Espacial

A complexidade espacial é quanto de espaço na memória será necessário para executar o algoritmo.
Se você está procurando um bit na memória, não importa o tamanho do array, você só vai precisar alocar 1 bit de memória para isso. O(1).

## O(1) - Constant Time:

``` Python
#python
def get_first_element(arr): return arr[0]
```
Não importa o tamanho do array, o tempo de execução desse código sempre será o mesmo. portanto O(1).

## O(log n) - Logarithmic time:

Uma função de busca binária por um elemento especifico em um array ordenado.

Se o elemento for 2, por exemplo, teriamos:

[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]<br>

A busca binária vai ao meio do array arr[5] e vai verificar se o valor que lá está é maior ou menor que 2. se for maior, ela vai ignorar o lado direito da lista (o lado de valores maiores) e vai novamente dividir a metade o array da parte menor, indo para posição arr[3] ou arr[2]. Caso vá para a posição arr[3], ele vai precisar fazer mais uma execução. Caso vá direto para o arr[2], ele encerra a execução.
Ou seja, seria necessário entre 2 a 3 execuções.

Caso o array fosse de 20 elementos:
[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, . . ., 20]<br>
A primeira metade seria a arr[10]
Depois a arr[5]
Depois a arr[3] ou arr[2]
Ou seja, seria necessário entre 3 a 4 execuções.

O array DOBROU de tamanho, mas o numero de execuções aumentou em apenas 1.

log2(10) = 3.321
log2(20) = 4.321
log2(40) = 5.321

## O(n) - Linear Time:

Conforme o input aumenta, o tempo de execução aumenta proporcionalmente.

Se a função por exemplo for identificar qual é o maior elemento daquele array, ele vai ter que percorrer todos os itens daquele array.

Portanto, vai demorar X para 10 elementos e 2X para 20 elementos.

## O(n log n) - Linearithmic time:

Ex: MergeSort

Uma parte do algoritmo escala com log(n) e outra escala apenas com n.

Um algoritmo que divida na metade o numero de elementos e procure em uma das listas o maior valor armazenado, depois divide na metade novamente e percorre a procura do maior valor novamente, e repete isso até não ter mais como dividir por 2. A complexidade seria n log(n), porque quanto maior o array, mais tempo de percorrimento, mas também ao dividir pela metade para procurar o valor seria por log(n).

basicamente uma parte escala com log(n) e outra com n.

## O(n^2) - Quadratic Time:

Um loop do array dentro de outro loop do mesmo array:
```Python
# Python
for i in range(n)
    for j in range (n)
```
Imagine que vamos tentar fazer combinações de todos os elementos do array, usando duplas.
[1, 2, 3, 4, 5, 6, 7, 8, 9]
Assim teriamos:
- 12
- 13
- 14
- 15
- ...
Portanto, com 10 elementos, a execução é 10x10, porque vai combinar todos os elementos com todos os elementos. 10x10 é 10^2.

Se o array tiver 100 posições, então será 100x100, 100^2. e não apenas 10 vezes maior (10 x 10 = 100).

## O(2^n) - Exponential Time:

```Python
#python
def fibonacci(n):
    if n <= 1:
        return n
    else:
        return fibonacci(n-1) + fibonacci(n-2)
```
Para cada item novo adicionado no input, o tempo de execução será dobrado.

O(2^n) onde o n = numero de elementos (4) demora x.
Se o n passa a ser 5, demora 2x.

## O(n!) - Factorial Time:

Gerar todas as permutações entre o array.

[1, 2] = 1 - 2 - 12 - 21
[1, 2, 3] = 1 - 3 - 12 - 21 - 13 - 31 - 23 - 32

Para cada novo item, aumenta fatorialmente o tempo de execução.

## OBSERVAÇÕES

Sempre ser pessimista referente ao tempo de execução, considerar que em uma busca de um item em uma lista, ele sempre estará na ultima posição, ou seja, percorrendo o array inteiro.