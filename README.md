# Java script 
---


# Variáveis 

- Em javascript temos 3 tipos de variáveis, **let**, **var**, e **const**. Usamos cada uma delas em situações diferentes:

  - **CONST**: Pode ser usado em qualquer situação, menos se estiver redefinindo uma variável.
  - **LET**: Utilizado quando se está trabalhando com loops.
  - **VAR**: Usado somente em casos especificos como: se você estiver trabalhando em código legado, você precisa redeclarar uma variável, ou você precisa de uma variável global.

## Como declarar uma variável
 Para declarar uma variável utilizamos a seguinte sintaxe:
```java scripr
 let ou var [identidicador] = [valor ou expressão] 
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
```
- Existem três tipos de escopo:
  - Global: É o escopo mais amplo do codigo, com funções definidas fora de qualquer outra função ou bloco. No exemplo acima a função 1 tem um escopo global.
  -  

 