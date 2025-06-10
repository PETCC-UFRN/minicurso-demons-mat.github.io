---
date: 2025-06-07 12:26:40
layout: post
title: Demonstrações e Lean | Dia 4
subtitle: Se aprofundando em Demonstrações Matemáticas e entendendo a praticidade dos provadores de teoremas.
description: Nesse dia iremos nos aprofundar nos diferentes tipos de demonstrações matemáticas e como utilizar o provador de teoremas Lean.
#image: https://res.cloudinary.com/dm7h7e8xj/image/upload/v1559822138/theme9_v273a9.jpg
#optimized_image: https://res.cloudinary.com/dm7h7e8xj/image/upload/c_scale,w_380/v1559822138/theme9_v273a9.jpg
category: Math
tags:
  - Demonstrações Matemáticas
  - Provadores de teoremas
  - Lean
author: PET-CC
paginate: true
---

## As diferentes formas de demonstração:


Existem diferentes maneiras de se demonstrar algo na matemática, e podemos dividí-las em algumas categorias para facilitar nosso aprendizado.

### Demonstração por força bruta:


O método mais simples para demonstrações pequenas, que dependem de poucos casos específicos.

> Exemplo: demonstrar que todos os membros do conjunto de naturais {1, 3, 15,78, 6, 4, 2} são menores do que 80.

Imagine ter que demonstrar uma propriedade para um conjunto de 500 mil elementos!

Como conseguiriamos utilizar isso para demonstrar uma propriedade de um conjunto infinito? Spoiler: Não dá!

### Demonstração direta:


É chamada de demonstração direta quando conseguimos demonstrar o nosso alvo apenas utilizando os quantificadores em sua forma “padrão” e os dados que temos ou obtivemos.


> Exemplo: utilizar de exemplo alguma demonstração simples feita no dia 3 sobre conjuntos.


### Demonstração por escolha ou contra-exemplo:


Para lidar com o quantificador do existêncial (∃), basta escolhermos alguém que satisfaça suas condições necessárias. A mesma coisa acontece quando queremos demonstrar a negação ou refutar um para todo (∀), basta escolhermos um contra-exemplo que **não** satisfaça tais propriedades. 

> Exemplo: (∃p ∈ Primos)[p par]

> Exemplo: (∀ p ∈ Primos)[p ímpar];

### Demonstração por contradição (BOOM!):


Imagine que apartir de uma hipotese seja possível de chegar na conclusão de que 0 = 1? Assim é chamada a demonstração por contradição. Tendo nossas hipotéses, podemos supor por contradição que o alvo é falso e tentar chegar a algo claramente falso.

>Exemplo: -INCOMPLETO-

## Ferramentas de Proof Assistant e Introdução ao Lean

Já pensou se nossas demonstrações matemáticas fossem cercadas de incertezas, e se pudessem estar erradas por causa de erros ou desvios? Quais seriam as consequências disso nas aplicações que dependem dessas demonstrações? BOOM!

Foi a partir dessas dúvidas que surgiram ferramentas que ajudam nas demonstrações matemáticas — os chamados Proof Assistants, ou provadores de teoremas.

O provador de teoremas que vamos usar se chama Lean, um sistema criado no Brasil e que hoje é utilizado pela comunidade matemática internacional.

O Lean é uma linguagem de programação que funciona tanto como linguagem funcional quanto como provador de teoremas.


### Lean Overview

Sabe toda aquela conversa sobre alvo, dados e hipóteses? O Lean tem uma aba de visão geral que ajuda bastante, mostrando qual é o alvo a ser demonstrado, os dados disponíveis, as hipóteses e as variáveis que estão no escopo.

>PRINT MOSTRANDO O OVERVIEW DO LEAN.

>Talvez pedir para os alunos abrirem o live-lang para verem o Lean Overview funcionando(?).

### Quantificadores em Lean

Em Lean, os quantificadores funcionam da mesma maneira na qual foram abordados anteriormente.

> PRINT MOSTRANDO A CARA DE UMA DEMONSTRAÇÃO EM LEAN, COM FOCO NOS QUANTIFICADORES.

### Lean tactics

As táticas do Lean são os "comandos" utilizados nas demonstrações. A ideia é bem parecida com o que fizemos até então nas demonstrações feitas em sala. Para cada quantificador, temos maneiras diferentes de atacá-los ou utilizá-los. Algumas táticas também são utilizadas para criarmos novos dados e terminar a demonstração.

#### intro:
`intro` é a maneira de atacar um alvo da forma (∀). Numa demonstração feita no papel escreveríamos "Seja x".
```lean
example : ∀ (x : α) (A : Set α), x ∈ A → x ∈ A := by {
 intro x
 intro A
 intro h
 exact h
}
```
#### exact:
`exact _` é a principal maneira de terminar uma demonstração. Quando temos em nossos dados a coisa que queremos demonstrar, usamos `exact (hipótese)`.

#### use:
`use` é a maneira de atacar um alvo de forma (∃). Numa demonstração no papel diríamos "uso x".
```lean
example : ∃ x : Nat, x ∈ {n | n > 0} := by {               
use 1
exact Nat.one_pos  
}
```
>Nat.one_pos é o axioma que define que o natural 1 é maior que o natural 0.

#### have:
`have` é a maneira de criar um dado novo utilizando dados que já temos. Note que você não pode "criar" um dado do nada, precisa demonstrá-lo!
```lean
example {α} : ∀ (x : α ) (A B C : Set α ), A ⊆ B → B ⊆ C → x ∈ A → x ∈ C := by {
intro x
intro A B C
intro h1
intro h2
intro h3

have h4 : x ∈ B := h1 h3
have h5 : x ∈ C := h2 h4
exact h5
}
```
A sintaxe funciona da seguinte maneira:

`nome_da_hipótese : hipótese := demonstração`

#### rw[_]:
Quando queremos substituir algo no nosso alvo ou em alguma hipótese por algo que já temos nos nossos dados, podemos usar a tática `rw [dado]`, que reescreve o alvo ou a hipótese.
```lean
example {α} : ∀ (x : α) (A B : Set α), B = A → x ∈ A → x ∈ B := by {
intro x
intro A B
intro hipotese.BA
intro hipotese.A
rw[hipotese.BA]
exact hipotese.A
}
```

#### apply:
`apply` é a tática que serve para aplicarmos uma hipótese em nosso alvo ou em outra hipótese, mudando sua forma.

```lean
example {α} : ∀ (x : α ) (A B C : Set α ), A ⊆ B → B ⊆ C → x ∈ A → x ∈ C := by {
intro x
intro A B C
intro h1
intro h2
intro h3

apply h2
apply h1
exact h3
}
```


Etiam porta **sem malesuada magna** mollis euismod. Cras mattis consectetur purus sit amet fermentum. Aenean lacinia bibendum nulla sed consectetur.

<!--page-->

## Inline HTML elements

HTML defines a long list of available inline tags, a complete list of which can be found on the [Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/HTML/Element).

- **To bold text**, use `<strong>`.
- *To italicize text*, use `<em>`.
- Abbreviations, like <abbr title="HyperText Markup Langage">HTML</abbr> should use `<abbr>`, with an optional `title` attribute for the full phrase.
- Citations, like <cite>&mdash; Thomas A. Anderson</cite>, should use `<cite>`.
- <del>Deleted</del> text should use `<del>` and <ins>inserted</ins> text should use `<ins>`.
- Superscript <sup>text</sup> uses `<sup>` and subscript <sub>text</sub> uses `<sub>`.

Most of these elements are styled by browsers with few modifications on our part.

<!--page-->

# Heading 1

## Heading 2

### Heading 3

#### Heading 4

Vivamus sagittis lacus vel augue rutrum faucibus dolor auctor. Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit. Morbi leo risus, porta ac consectetur ac, vestibulum at eros.

## Code

Cum sociis natoque penatibus et magnis dis `code element` montes, nascetur ridiculus mus.

```lean
example : ∀ (x : U) (A : Set U), x ∈ A → x ∈ A := by {
 intro x
 intro A
 intro h
 exact h
}
```

<!--page-->

Aenean lacinia bibendum nulla sed consectetur. Etiam porta sem malesuada magna mollis euismod. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa.

## Lists

Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus. Aenean lacinia bibendum nulla sed consectetur. Etiam porta sem malesuada magna mollis euismod. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.

* Praesent commodo cursus magna, vel scelerisque nisl consectetur et.
* Donec id elit non mi porta gravida at eget metus.
* Nulla vitae elit libero, a pharetra augue.

Donec ullamcorper nulla non metus auctor fringilla. Nulla vitae elit libero, a pharetra augue.

1. Vestibulum id ligula porta felis euismod semper.
2. Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
3. Maecenas sed diam eget risus varius blandit sit amet non magna.

<!--page-->

Cras mattis consectetur purus sit amet fermentum. Sed posuere consectetur est at lobortis.

Integer posuere erat a ante venenatis dapibus posuere velit aliquet. Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Nullam quis risus eget urna mollis ornare vel eu leo.

## Images

Quisque consequat sapien eget quam rhoncus, sit amet laoreet diam tempus. Aliquam aliquam metus erat, a pulvinar turpis suscipit at.

![placeholder](https://placehold.it/800x400 "Large example image")
![placeholder](https://placehold.it/400x200 "Medium example image")
![placeholder](https://placehold.it/200x200 "Small example image")

## Tables

Aenean lacinia bibendum nulla sed consectetur. Lorem ipsum dolor sit amet, consectetur adipiscing elit.

<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Upvotes</th>
      <th>Downvotes</th>
    </tr>
  </thead>
  <tfoot>
    <tr>
      <td>Totals</td>
      <td>21</td>
      <td>23</td>
    </tr>
  </tfoot>
  <tbody>
    <tr>
      <td>Alice</td>
      <td>10</td>
      <td>11</td>
    </tr>
    <tr>
      <td>Bob</td>
      <td>4</td>
      <td>3</td>
    </tr>
    <tr>
      <td>Charlie</td>
      <td>7</td>
      <td>9</td>
    </tr>
  </tbody>
</table>

<!--page-->

Nullam id dolor id nibh ultricies vehicula ut id elit. Sed posuere consectetur est at lobortis. Nullam quis risus eget urna mollis ornare vel eu leo.










