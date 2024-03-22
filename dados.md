
# Dados

## Objeto
- Objetos são coleções de dados, como se fossem objetos da vida real, com caractericas e atributos. Como um cachorro, qual sua raça, sua cor, seu nome, etc.

```javascript
var cachorro = {
  nome: "Bob",
  sexo: "macho",
  raca: "golden retriver",
}

console.log(cachorro.nome) // retornara o nome do cachorro 
```

## Array
- São obejtos semelhantes a uma lista. 

```javascript
var a = ["primeiro elemento", "segundo elemento"];
console.log(a[0]); // exibe 'primeiro elemento'
console.log(a[1]); // exibe 'segundo elemento'
```


---
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