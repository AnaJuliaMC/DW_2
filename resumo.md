# Resumo de JavaScript

## String

Uma string é uma sequência de caracteres. Em JavaScript, podemos criar strings de várias maneiras:

- Usando aspas simples (`'`) ou duplas (`"`)
- Usando template strings (\``)

As strings são imutáveis em JavaScript, o que significa que não podem ser alteradas após a criação. Algumas operações comuns em strings incluem `split()`, `replace()` e `slice()`. Também podemos converter strings em números e vice-versa.
# Template string
Template strings, também conhecidos como template literals, são uma característica do JavaScript que permite a criação de strings multi-linhas de forma mais legível e com capacidade de interpolação de variáveis diretamente dentro da string.

Em JavaScript, os template strings são definidos utilizando crases (`) em vez de aspas simples ou duplas. Por exemplo:

```javascript
const nome = 'João';
const idade = 30;

const mensagem = `Olá, meu nome é ${nome} e tenho ${idade} anos.`;

console.log(mensagem);

```

# split

A função `split()` em JavaScript é usada para dividir uma string em um array de substrings com base em um separador especificado. Aqui está a sintaxe básica:

```javascript
string.split(separador, limite);
```

- `string`: A string que você deseja dividir.
- `separador` (opcional): O caractere ou expressão regular que indica onde a string deve ser dividida. Se este parâmetro for omitido, a string será dividida em substrings individuais a cada caractere.
- `limite` (opcional): Um número inteiro que especifica o número máximo de divisões a serem feitas. As divisões são feitas da esquerda para a direita. Se o parâmetro limite for omitido, todas as divisões possíveis são feitas.

Exemplo simples:

```javascript
const str = "Olá, mundo!";
const array = str.split(','); // Divide a string onde encontrar vírgulas
console.log(array); // Saída: ["Olá", " mundo!"]
```

Exemplo com limite:

```javascript
const str = "a,b,c,d,e";
const array = str.split(',', 3); // Divide a string usando vírgulas, com limite de 3 divisões
console.log(array); // Saída: ["a", "b", "c"]
```

Se o separador for uma string vazia (`''`), cada caractere da string será separado individualmente. Isso é útil para converter uma string em um array de caracteres:

```javascript
const str = "abcdef";
const array = str.split('');
console.log(array); // Saída: ["a", "b", "c", "d", "e", "f"]
```

A função `split()` é amplamente utilizada em JavaScript para dividir strings com base em diferentes critérios, tornando mais fácil manipular e trabalhar com os dados em formato de array.

# Função `replace()` em JavaScript

A função `replace()` em JavaScript é usada para substituir partes de uma string por outra string ou valor. Aqui está a sintaxe básica:

```javascript
string.replace(valorOuExpressao, novaStringOuFuncao);
```


- \`string\`: A string na qual você deseja fazer a substituição.
- \`valorOuExpressao\`: O valor ou expressão regular que você deseja substituir na string. Pode ser uma string ou uma expressão regular.
- \`novaStringOuFuncao\`: A string que substituirá o valor ou uma função que retorna a nova substring.

## Exemplo simples substituindo uma substring por outra:

```javascript
const str = "Olá, mundo!";
const novaStr = str.replace('mundo', 'Planeta');
console.log(novaStr); // Saída: "Olá, Planeta!"
```

Neste exemplo, "mundo" foi substituído por "Planeta".

## Substituições avançadas com expressões regulares:

```javascript
const str = "JavaScript é legal!";
const novaStr = str.replace(/(JavaScript) (é) (legal)/, '$1 não $2 tão $3');
console.log(novaStr); // Saída: "JavaScript não é tão legal!"
```

Neste exemplo, a expressão regular captura as três partes da frase e as usa para criar uma nova frase com a palavra "não" adicionada antes de "é" e "tão" antes de "legal".

## Substituições dinâmicas com funções:

```javascript
function substituirTexto(match, p1, p2, p3, offset, stringOriginal) {
  return `${p1.toUpperCase()} ${p2.toUpperCase()} ${p3.toUpperCase()}`;
}

const str = "programação é divertida!";
const novaStr = str.replace(/(programação) (é) (divertida)/, substituirTexto);
console.log(novaStr); // Saída: "PROGRAMAÇÃO É DIVERTIDA"
```

Neste exemplo, a função \`substituirTexto\` recebe as partes capturadas pela expressão regular e retorna uma nova string com as partes em maiúsculas.

A função \`replace()\` é uma ferramenta poderosa em JavaScript para manipulação de strings, permitindo substituições simples ou avançadas com expressões regulares e funções.

# Função `slice()` em JavaScript

A função `slice()` em JavaScript é usada para extrair uma parte de uma string e retornar essa parte como uma nova string, sem modificar a string original. Aqui está a sintaxe básica:

```javascript
string.slice(inicio, fim);
```

- \`string\`: A string da qual você deseja extrair uma parte.
- \`inicio\`: O índice onde a extração deve começar. Se omitido, a extração começará do início da string.
- \`fim\`: O índice antes do qual a extração deve parar. Se omitido, a extração irá até o final da string.

## Exemplo simples de uso:

```javascript
const str = "abcdefgh";
const parte = str.slice(2, 5);
console.log(parte); // Saída: "cde"
```

Neste exemplo, a parte da string começando no índice 2 e indo até o índice 4 (exclusivo) é extraída.

A função \`slice()\` é útil para trabalhar com substrings em JavaScript, permitindo a extração de partes específicas de uma string sem modificar a original.

---

# Função `indexOf()` em JavaScript

A função `indexOf()` em JavaScript é usada para encontrar a primeira ocorrência de um valor especificado dentro de uma string. Aqui está a sintaxe básica:

```javascript
string.indexOf(valor, indiceInicial);
```

- \`string\`: A string na qual você deseja procurar.
- \`valor\`: O valor que você deseja encontrar dentro da string.
- \`indiceInicial\` (opcional): O índice a partir do qual a busca deve começar. Se omitido, a busca começará do início da string.

## Exemplo simples de uso:

```javascript
const str = "abcdefgh";
const indice = str.indexOf("e");
console.log(indice); // Saída: 4
```

Neste exemplo, o índice da primeira ocorrência de "e" na string é retornado.

A função \`indexOf()\` é comumente usada para verificar a presença de um caractere ou substring em uma string e encontrar a posição da primeira ocorrência.

---

# Função `lastIndexOf()` em JavaScript

A função `lastIndexOf()` em JavaScript é semelhante à função `indexOf()`, mas retorna a posição da última ocorrência de um valor especificado dentro de uma string. Aqui está a sintaxe básica:

```javascript
string.lastIndexOf(valor, indiceInicial);
```

- \`string\`: A string na qual você deseja procurar.
- \`valor\`: O valor que você deseja encontrar dentro da string.
- \`indiceInicial\` (opcional): O índice a partir do qual a busca deve começar, contando do final da string. Se omitido, a busca começará do final da string.

## Exemplo simples de uso:

```javascript
const str = "abcdefghde";
const indice = str.lastIndexOf("d");
console.log(indice); // Saída: 8
```

Neste exemplo, o índice da última ocorrência de "d" na string é retornado.

A função \`lastIndexOf()\` é útil para encontrar a posição da última ocorrência de um caractere ou substring em uma string.



## Funções

As funções são blocos de código que podem ser chamados para executar uma tarefa específica. Existem diferentes maneiras de definir funções em JavaScript:

- Como declaração: `function nomeFuncao() {}`
- Como expressão: `const nomeFuncao = function() {}`
- Usando arrow functions: `const nomeFuncao = () => {}`

# Function Declaration em JavaScript

Em JavaScript, funções podem ser declaradas de várias maneiras. Uma delas é através da declaração de função, também conhecida como "function declaration". Aqui está um exemplo simples de como declarar uma função em JavaScript:

```javascript
function minhaFuncao(parametro1, parametro2) {
    // Corpo da função
    // Aqui você escreve o código que a função executará
    console.log(parametro1 + parametro2);
}
 # Function Expression e Arrow Function em JavaScript

## Function Expression

Além da declaração de função, você também pode criar funções usando uma expressão de função, chamada de "function expression". Aqui está um exemplo:

```javascript
const minhaFuncao = function(parametro1, parametro2) {
    console.log(parametro1 + parametro2);
};
```

Neste exemplo:
- \`minhaFuncao\` é uma variável que armazena a função.
- \`function(parametro1, parametro2)\` é a expressão de função.
- O corpo da função vem após a expressão de função.

Você pode chamar a função da mesma maneira que faria com uma função declarada:

```javascript
minhaFuncao(2, 3); // Saída: 5
```

## Arrow Function

As Arrow Functions são uma forma mais concisa de escrever funções em JavaScript, introduzidas no ECMAScript 6. Aqui está um exemplo de uma Arrow Function:

```javascript
const minhaArrowFunction = (parametro1, parametro2) => {
    console.log(parametro1 + parametro2);
};
```

Neste exemplo:
- \`minhaArrowFunction\` é uma variável que armazena a Arrow Function.
- \`(\parametro1, parametro2)\` são os parâmetros da função.
- \`=>\` é a sintaxe da Arrow Function.
- O corpo da função vem após a seta \`=>\`.

Você pode chamar a Arrow Function da mesma maneira que faria com outras funções:

```javascript
minhaArrowFunction(2, 3); // Saída: 5
```

As Arrow Functions têm algumas diferenças em relação às funções regulares, como a ligação do contexto (\`this\`) e a sintaxe mais compacta, tornando-as úteis em muitos casos, especialmente para funções simples e callbacks.


## Objeto

Um objeto é uma coleção de pares de chave-valor. Podemos criar objetos usando a sintaxe de objeto literal (`{}`) e definir atributos usando a notação ponto (`.`) ou a notação de colchetes. O operador de desestruturação também é útil para extrair valores de objetos.

# Criando um objeto

Em JavaScript, você pode criar objetos de várias maneiras. Um objeto é uma coleção de pares de chave e valor. Aqui está um exemplo simples de como criar um objeto:

```javascript
const meuObjeto = {};
```

Este é um objeto vazio. Você pode adicionar propriedades a este objeto usando diferentes métodos.

## Definindo atributo com a notação ponto (.)

Você pode adicionar propriedades a um objeto usando a notação ponto. Aqui está um exemplo:

```javascript
meuObjeto.nome = "John";
meuObjeto.idade = 30;
```

Aqui, estamos adicionando propriedades \`nome\` e \`idade\` ao objeto \`meuObjeto\` usando a notação ponto.

## Definindo atributo com a notação chave-valor

Você também pode adicionar propriedades a um objeto usando a notação chave-valor. Aqui está um exemplo:

```javascript
meuObjeto['endereco'] = '123 Main Street';
meuObjeto['cidade'] = 'New York';
```

Desta vez, estamos usando a notação de colchetes e strings como chaves para adicionar propriedades ao objeto.

## Operador de desestruturação em um objeto

O operador de desestruturação em JavaScript permite extrair valores de objetos e atribuí-los a variáveis individuais. Aqui está um exemplo de como usar o operador de desestruturação em um objeto:

```javascript
const { nome, idade } = meuObjeto;
console.log(nome); // Saída: "John"
console.log(idade); // Saída: 30
```

Neste exemplo, estamos extraindo os valores das propriedades \`nome\` e \`idade\` do objeto \`meuObjeto\` e atribuindo-os às variáveis \`nome\` e \`idade\`.

Estas são algumas das maneiras de criar e trabalhar com objetos em JavaScript, permitindo armazenar e manipular dados de forma organizada e eficiente.


## Array

Um array é uma coleção ordenada de elementos. Podemos criar arrays usando a sintaxe de array literal (`[]`) e usar uma variedade de métodos para adicionar, remover e modificar elementos, como `push()`, `pop()`, `slice()`, entre outros. Os operadores de desestruturação também podem ser usados com arrays.


## Formas de criar um array

Existem várias formas de criar um array em JavaScript:

- Utilizando colchetes `[]` e inserindo os elementos manualmente.
- Utilizando o construtor `new Array()` e especificando os elementos como argumentos.

Exemplo:
```javascript
// Criando um array manualmente
let array1 = [1, 2, 3];

// Criando um array utilizando o construtor
let array2 = new Array(1, 2, 3);
```

# Função push() em JavaScript

A função `push()` é um método utilizado em arrays em JavaScript para adicionar um ou mais elementos ao final do array. Ela modifica o array original e retorna o novo comprimento do array.

## Sintaxe

```javascript
array.push(elemento1, elemento2, ..., elementoN)

let array = [1, 2, 3];
array.push(4, 5);
// Agora array é [1, 2, 3, 4, 5]
```
# Função pop() em JavaScript

A função `pop()` é um método utilizado em arrays em JavaScript para remover o último elemento do array. Ela modifica o array original e retorna o elemento removido.

## Sintaxe

```javascript
array.pop()

let array = [1, 2, 3];
let elementoRemovido = array.pop();
// Agora array é [1, 2] e elementoRemovido é 3
```

# Função shift() em JavaScript

A função `shift()` é um método utilizado em arrays em JavaScript para remover o primeiro elemento do array. Ela modifica o array original e retorna o elemento removido.

## Sintaxe

```javascript
array.shift()

let array = [1, 2, 3];
let elementoRemovido = array.shift();
// Agora array é [2, 3] e elementoRemovido é 1
```

# Função unshift() em JavaScript

A função `unshift()` é um método utilizado em arrays em JavaScript para adicionar um ou mais elementos ao início do array. Ela modifica o array original e retorna o novo comprimento do array.

## Sintaxe

```javascript
array.unshift(elemento1, elemento2, ..., elementoN)
let array = [3, 4, 5];
array.unshift(1, 2);
// Agora array é [1, 2, 3, 4, 5]
```

# Função splice() em JavaScript

A função `splice()` é um método utilizado em arrays em JavaScript para realizar operações de inserção, remoção e substituição de elementos em qualquer posição do array. Ela modifica o array original e retorna um novo array contendo os elementos removidos, ou um array vazio se nenhum elemento for removido.

## Sintaxe

```javascript
array.splice(inicio, quantidade[, elemento1[, elemento2[, ...]]])

let array = [1, 2, 3, 4, 5];
let elementosRemovidos = array.splice(2, 2, 'a', 'b', 'c');
// Agora array é [1, 2, 'a', 'b', 'c', 5] e elementosRemovidos é [3, 4]
```

# Função slice() em JavaScript

A função `slice()` é um método utilizado em arrays em JavaScript para retornar uma parte do array, sem modificar o array original. Ela retorna uma cópia rasa (shallow copy) dos elementos selecionados em um novo array.

## Sintaxe

```javascript
array.slice(inicio, fim)

let array = [1, 2, 3, 4, 5];
let novaArray = array.slice(1, 4);
// Agora novaArray é [2, 3, 4]
```

# Operador delete em JavaScript (para remoção de elementos de um array)

O operador `delete` em JavaScript é usado para remover uma propriedade de um objeto. Quando aplicado a elementos de um array, ele remove o valor do elemento, mas não o elimina fisicamente do array, deixando um "buraco" no lugar do elemento removido.

## Sintaxe

```javascript
delete array[indice]

let array = [1, 2, 3, 4, 5];
delete array[2];
// Agora array é [1, 2, <empty>, 4, 5]
```

# Função map() em JavaScript

A função `map()` é um método utilizado em arrays em JavaScript para iterar sobre cada elemento do array e aplicar uma função a cada elemento, retornando um novo array com os resultados das chamadas de função.

## Sintaxe

```javascript
array.map(funcaoAtual(elemento, indice, arrayOriginal), thisArg)

let numeros = [1, 2, 3, 4, 5];
let dobrados = numeros.map(function(numero) {
  return numero * 2;
});
// Agora dobrados é [2, 4, 6, 8, 10]
```

# Função filter() em JavaScript

A função `filter()` é um método utilizado em arrays em JavaScript para criar um novo array contendo apenas os elementos que passam por um teste especificado por uma função.

## Sintaxe

```javascript
array.filter(funcaoAtual(elemento, indice, arrayOriginal), thisArg)

let numeros = [1, 2, 3, 4, 5];
let numerosPares = numeros.filter(function(numero) {
  return numero % 2 === 0;
});
// Agora numerosPares é [2, 4]
```

# Função every() em JavaScript

A função `every()` é um método utilizado em arrays em JavaScript para verificar se todos os elementos do array passam por um teste específico implementado por uma função. Retorna true se todos os elementos passam no teste ou false se pelo menos um elemento não passa.

## Sintaxe

```javascript
array.every(funcaoAtual(elemento, indice, arrayOriginal), thisArg)

let numeros = [1, 2, 3, 4, 5];
let todosMaioresQueZero = numeros.every(function(numero) {
  return numero > 0;
});
// Agora todosMaioresQueZero é true
```

# Operador de Desestruturação de Array em JavaScript

O operador de desestruturação de array é uma forma de extrair valores de arrays e atribuí-los a variáveis em uma única expressão, de maneira concisa e elegante.

## Sintaxe

```javascript
let [variavel1, variavel2, ..., variavelN] = array;

let numeros = [1, 2, 3];
let [primeiro, segundo, terceiro] = numeros;
console.log(primeiro); // Saída: 1
console.log(segundo); // Saída: 2
console.log(terceiro); // Saída: 3
```



## Operadores

Os operadores são símbolos que realizam operações em operandos. Alguns operadores comuns em JavaScript incluem o operador ternário (`? :`) e os operadores Spread (`...`) e Rest (`...args`), usados principalmente com arrays e objetos.

# Operador Ternário em JavaScript

O operador ternário é uma forma concisa de escrever instruções condicionais em JavaScript. Ele permite avaliar uma expressão e retornar um valor com base nessa avaliação.

## Sintaxe

```javascript
condicao ? expressao1 : expressao2

let idade = 20;
let mensagem = idade >= 18 ? 'Maior de idade' : 'Menor de idade';
console.log(mensagem); // Saída: "Maior de idade"
```

# Operador Spread e Operador Rest em JavaScript

Os operadores spread e rest são recursos poderosos do JavaScript que oferecem flexibilidade na manipulação de arrays e objetos.

## Operador Spread (Spread Operator)

O operador spread (`...`) é utilizado para expandir um array ou objeto em múltiplos elementos.

### Sintaxe

```javascript
// Expansão de array
let novoArray = [...arrayExistente];

// Expansão de objeto
let novoObjeto = {...objetoExistente};


let array1 = [1, 2, 3];
let array2 = [4, 5, 6];
let novoArray = [...array1, ...array2];
// novoArray agora é [1, 2, 3, 4, 5, 6]

//REST!!!!
// Agrupamento de argumentos em uma função
function minhaFuncao(parametro1, parametro2, ...restoDosParametros) {
  // ...
}

// Agrupamento de elementos em um array
let [primeiro, segundo, ...restoDoArray] = arrayExistente;


function soma(...numeros) {
  return numeros.reduce((total, numero) => total + numero, 0);
}

console.log(soma(1, 2, 3, 4, 5)); // Saída: 15

let numeros = [1, 2, 3, 4, 5];
let [primeiro, segundo, ...restoDoArray] = numeros;
console.log(restoDoArray); // Saída: [3, 4, 5]


//Spread
function mostraSoma(a, b, c) {
    console.log(a + b + c);
}

let elementos = [2, 4, 6];

mostraSoma(1, 2, 3)      // 6
mostraSoma(...elementos) // 12

let itens = ["banana", "maça"]
let lista = ["pera", ...itens, "uva"]
console.log(lista) // ["pera", "banana", "maça", "uva"]

let vet1 = [1,2,3]
let vet2 = [4,5]
let vet3 = [...vet1, ...vet2]
console.log(vet3)  // [1,2,3,4,5]



//Rest
function testandoRest1(a, b, ...argumentos) {
    console.log(a, b, argumentos)  // 1, 2, [3,4,5]
}

function testandoRest2(...argumentos) {
    console.log(argumentos)        // [1,2,3,4,5]
}

testandoRest1(1,2,3,4,5)
testandoRest2(1,2,3,4,5)
```
