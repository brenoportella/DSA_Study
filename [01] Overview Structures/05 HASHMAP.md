```Python
#python
{}.get("augusto") => "azul"
```
Basicamente uma forma de transformar o input de pesquisa (augusto) em um numero único que seja exato a posição do array onde o valor desejado (azul) está armazenado.
Em python é chamado de dictionary.

Hashmap usa uma HASH FUNCTION para transformar a string em um numero gigante (MD5 ou SHA-256) e depois fazer um modulo (%) pelo tamanho de elementos do array. Assim tendo uma posição especifica dele no array.

Porém existem dois fatores importantes quando se trata de um *hashmap* que são:

### Load Factor
Basicamente o quão cheio está aquele array com bytes diferentes de nulos. Ou seja, o quanto tem de espaço disponível para alocar informações e evitar colisões de informações.

### Collisions
Quando dois elementos são alocados no mesmo endereço, gerando um overwrite.

Lidar com as *Collisions* requer um protocolo de respeitar um percentual de *Load Factor* ideal para o projeto. Geralmente em 70%. Além disso existem duas formas de lidar com uma *collision*. Uma delas é armazenando na memória a Chave (key) e o valor (value) e caso algum valor diferente queira ser armazenado no espaço que já está sendo utilizado, ele vai procurar o próximo espaço livre para armazena-lo.
O que pode ser um problema a depender do tamanho do array e *load factor*.
Ou gerar uma pequena lista de itens naquele espaço, onde a busca pelo valor(value) seria através de um loop (o(n)) para encontra-lo.
Importante: essa lista não pode ser grande, se não perdemos performance. Caso a lista seja pequena, logo a operação como um todo pode ser considerada O(1), já que a lista é pequena e o (O(n)) dela será muito irrelevante em termos de tempo para a execução.