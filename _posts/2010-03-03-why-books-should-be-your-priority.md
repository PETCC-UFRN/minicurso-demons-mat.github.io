---
date: 2018-11-22 12:26:40
layout: post
title: Demonstrações e Lean | Dia 4
subtitle: Lorem ipsum dolor sit amet, consectetur adipisicing elit.
description: Nesse dia iremos nos aprofundar nos diferentes tipos de demonstrações matemáticas e como utilizar o provador de teoremas Lean.
#image: https://res.cloudinary.com/dm7h7e8xj/image/upload/v1559822138/theme9_v273a9.jpg
#optimized_image: https://res.cloudinary.com/dm7h7e8xj/image/upload/c_scale,w_380/v1559822138/theme9_v273a9.jpg
category: life
tags:
  - Demonstrações Matemáticas
  - Provadores de teoremas
  - Lean
author: mranderson
paginate: true
---

## As diferentes formas de demonstração:


Cas sociis natoque penatibus et magnis <a href="#">dis parturient montes</a>, nascetur ridiculus mus. *Aenean eu leo quam.* Pellentesque ornare sem lacinia quam venenatis vestibulum.
### Método de Demonstração 1:


Cas sociis natoque penatibus et magnis <a href="#">dis parturient montes</a>, nascetur ridiculus mus. *Aenean eu leo quam.* Pellentesque ornare sem lacinia quam venenatis vestibulum.

> Exemplo: (∀p legal)[p legal ⇒ p maneiro].

### Método de Demonstração 2:


Cas sociis natoque penatibus et magnis <a href="#">dis parturient montes</a>, nascetur ridiculus mus. *Aenean eu leo quam.* Pellentesque ornare sem lacinia quam venenatis vestibulum.

> Exemplo: (∀ a : Person)(∃b : Person)[a gosta de b].

### Método de Demonstração 3:


Cas sociis natoque penatibus et magnis <a href="#">dis parturient montes</a>, nascetur ridiculus mus. *Aenean eu leo quam.* Pellentesque ornare sem lacinia quam venenatis vestibulum.

> Exemplo: (∃x natalense)[x curte calcinha preta]

### Método de Demonstração 4:


Cas sociis natoque penatibus et magnis <a href="#">dis parturient montes</a>, nascetur ridiculus mus. *Aenean eu leo quam.* Pellentesque ornare sem lacinia quam venenatis vestibulum.

## Ferramentas de Proof Assistant e Introdução ao Lean

Cas sociis natoque penatibus et magnis <a href="#">dis parturient montes</a>, nascetur ridiculus mus. *Aenean eu leo quam.* Pellentesque ornare sem lacinia quam venenatis vestibulum.

### Lean Overview

Cas sociis natoque penatibus et magnis <a href="#">dis parturient montes</a>, nascetur ridiculus mus. *Aenean eu leo quam.* Pellentesque ornare sem lacinia quam venenatis vestibulum.

### Quantificadores em Lean

Cas sociis natoque penatibus et magnis <a href="#">dis parturient montes</a>, nascetur ridiculus mus. *Aenean eu leo quam.* Pellentesque ornare sem lacinia quam venenatis vestibulum.

### Lean tactics

Cas sociis natoque penatibus et magnis <a href="#">dis parturient montes</a>, nascetur ridiculus mus. *Aenean eu leo quam.* Pellentesque ornare sem lacinia quam venenatis vestibulum.

#### Intro:
Etiam porta **sem malesuada magna** mollis euismod. Cras mattis consectetur purus sit amet fermentum.
```lean
example : ∀ (x : U) (A : Set U), x ∈ A → x ∈ A := by {
 intro x
 intro A
 intro h
 exact h
}
```
#### use:
Etiam porta **sem malesuada magna** mollis euismod. Cras mattis consectetur purus sit amet fermentum.
```lean
example : ∀ (x : U) (A : Set U), x ∈ A → x ∈ A := by {
 intro x
 intro A
 intro h
 exact h
}
```
#### have:
Etiam porta **sem malesuada magna** mollis euismod. Cras mattis consectetur purus sit amet fermentum.
```lean
example : ∀ (x : U) (A : Set U), x ∈ A → x ∈ A := by {
 intro x
 intro A
 intro h
 exact h
}
```
#### exact:
Etiam porta **sem malesuada magna** mollis euismod. Cras mattis consectetur purus sit amet fermentum.
```lean
example : ∀ (x : U) (A : Set U), x ∈ A → x ∈ A := by {
 intro x
 intro A
 intro h
 exact h
}
```
#### rw[]:
Etiam porta **sem malesuada magna** mollis euismod. Cras mattis consectetur purus sit amet fermentum.
```lean
example : ∀ (x : U) (A : Set U), x ∈ A → x ∈ A := by {
 intro x
 intro A
 intro h
 exact h
}
```
#### apply:
Etiam porta **sem malesuada magna** mollis euismod. Cras mattis consectetur purus sit amet fermentum.
```lean
example : ∀ (x : U) (A : Set U), x ∈ A → x ∈ A := by {
 intro x
 intro A
 intro h
 exact h
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










