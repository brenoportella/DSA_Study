# ARRAYS

Isso não é um array:
```javascript
//Javascript
let a = []
```

>**Um array é um espaço continuo de memória que pode ser interpretado como tendo vários elementos.**

Em teoria o array é o mesmo:

- 4 elementos de 4 bits
[0000 1111 0000 1111]

- 2 elementos de 8 bits
[00001111 00001111]

- 1 elemento de 16bits
[0000111100001111]

O array é o mesmo, mas o que muda é como interpretamos ele.

``` Rust
//RUST
let my_array: [i32; 4] = [1, 2, 3, 4];
```
Isso é a declaração de um array de 4 espaços para inteiros de 32 bits.

Como o array é uma lista sequencial de elementos, é complexo mudar o tamanho dele após a inicialização, pois ele necessita de que exista espaço sequencial suficiente para alocar todos os elementos do array, e fazer a realocação seria um processo de movimentação de memória tremendo, tornando tudo muito lento.
