### @ Em desenvolvimento 
# Programação Funcional
### Esse artigo usa como referência: 
- [Functional JavaScript, some concepts, by David Rey](https://dreyacosta.com/functional-javascript/); 
- [Functional Programming Principles in Javascript, by Leandro TK](https://medium.freecodecamp.org/functional-programming-principles-in-javascript-1b8fc6c3563f)
- [Functional Programming For Beginners With JavaScript, by James Moore](https://www.udemy.com/functional-programming-for-beginners-with-javascript/)

## Conceito 
Atualmente a programação funcional é um dos tópicos mais em alta no desenvolvimento de software. Javascript como uma linguagem flexivel, permite que programamos dessa forma. Você pode acompanhar os principais conceitos de programação funcional em javascript [aqui](/archives/plano-estudos.md).

### Imutabilidade
A imutabilidade é o conceito dados que não mudam após serem criados. Um exemplo de dado imutável no javascript é uma string. Quando você cria uma string em javascript ela não terá mais mudanças, você até pode usar a string para criar outras string, mas a original não terá mudanças.

```
    var test = 'testing...';
    test += 'test';
    console.log(test); // testing...test
```

### First-class (funções de primeira classe)
O conceito de first-class diz que qualquer coisa tem um valor. Por exemplo:

```
    var test = true
```

A programação funcional pode ser facilitada muito com o uso de funções de primeira-classe. Sendo que a função de primeira classe é uma função que pode fazer qualquer coisa com um valor. Para definir uma função de primeira classe em javascript é muito simples:

```
    var soma = function(a, b) {
        return a + b; 
    }
```

ou ainda

```
    var soma = (a, b) => a + b;
```

As funções de primeira classe também podem ser utilizadas para passar outras funções, dessa forma:

```
    var soma = (a, b) => a + b;
    var exec = (fn, a, b) => fn(a, b);
```