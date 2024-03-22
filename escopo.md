
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