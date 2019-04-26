### @ Em desenvolvimento 
# Imutabilidade
A imutabilidade é o conceito de dados que não mudam após serem criados. Um exemplo de dado imutável no javascript é uma string. Quando você cria uma string em javascript ela não terá mais mudanças, você até pode usar a string para criar outras string, mas a original não terá mudanças.

```
    var test = 'testing...';
    test += 'test';
    console.log(test); // testing...test
```

#### Objetos imutáveis
Aplicações em geral precisar alterar estados, por exemplo: 

```
const cadeira = {
   material: 'madeira'
};
```

Em determinado momento, poderá ser necessário adicionar um novo atributo, mas para que os dados se tornem imutáveis o correto seria copiar todos os atributos da cadeira adicionando apenas os novos:

```
const cadeira = {
   material: 'madeira'
};

const cadeiraAtualizada = {
   material: cadeira.material,
   cor: 'preto';
};
```

Porém em objetos com muitos atributos seria necessário copiar todos os atributos e a programação se tornaria extremamente verbosa, por isso usamos o [spread operator](https://developer.mozilla.org/pt-BR/docs/Web/JavaScript/Reference/Operators/Spread_operator):

```
const cadeira = {
   material: 'madeira'
};

const cadeiraAtualizada = {
   ...cadeira,
   cor: 'preto';
};
```

ou ainda para atualizar dados:

```
const cadeira = {
   material: 'madeira'
};

const cadeiraAtualizada = {
   ...cadeira,
   material: 'ferro',
   cor: 'preto';
};
```