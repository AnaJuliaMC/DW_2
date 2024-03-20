# Java script 
---


# Variáveis 

- Em javascript temos 3 tipos de variáveis, **let**, **var**, e **const**. Usamos cada uma delas em situações diferentes:

  - **CONST**: Pode ser usado em qualquer situação, menos se estiver redefinindo uma variável.
  - **LET**: Utilizado quando se está trabalhando com loops.
  - **VAR**: Usado somente em casos especificos como: se você estiver trabalhando em código legado, você precisa redeclarar uma variável, ou você precisa de uma variável global.

## Como declarar uma variável
 Para declarar uma variável utilizamos a seguinte sintaxe:
```javascript
 let ou var [identidicador] = [valor ou expressão] 
 console.log()
 ```
 Sendo identificador o nome da variável, e valor ou expressão o que será atribuido a ela.


## Escopo
 - Se refere a acessibilidade de variáveis e funções no codigo. Um escopo é criado toda vez que criamos uma função. Veja abaixo:
  ```javascript
  function função1(){
    //Aqui temos o escopo da função 1
    function função2(){
        //Aqui temos o escopo da função 2
    }
  }
  console.log()
```
- Existem três tipos de escopo:
  - Global: É o escopo mais amplo do codigo, com funções definidas fora de qualquer outra função ou bloco.
  - Função: é o escopo determinado pela criação de uma função, como vimos no exemplo acima.
  - Bloco: é o escopo de qualquer estrutura que utilize chaves, como: if, for, while, e etc. Abaixo temos um exemplo de escopo de bloco:

  ```javascript 
  function f1(){
    if (){
      //aqui teremos o escopo de bloco
    }
  }
  console.log()
  ```

# Tipos de dados

```javascript
let a = 13; // a sera um dado do tipo number
let a = 'dw'; // a sera um dado do tipo string
let a = true; // a sera um dado do tipo boolean
```
- **String:** são dados de cadeia de caracteres.
- **Number:** são dados usados para representar número, seja ele inteiro ou não.
- **Boolean:** são dados que representam apenas true e false e são usados em lógicas condicionais.
- **Null:** são dados que nãop tem valor.
- **Undefined:** é uma variavel que foi declarada porem nada foi atribuido a ela.

## Diferença entre null e undefined
- null é utilizado para indicar ausênsia de um objeto, e undefined ausencia de um valor.

- Para null temos:
  ```javascript
  const a = null;
  console.log(a)
  ```
- E para undefined temos:
  ```javascript
  const a;
  console.log(a)
  ``````
