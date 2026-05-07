# Análise de Problemas do HTML Sem Semântica e Soluções Aplicadas
##Diciplina
Desenvolvimento Web
## Alunos
Lara Geovana 22502104
Camilla Valenzuela 22502503
Gabriel Rios 22505812

## Descrição

Este repositório apresenta a análise comparativa entre duas versões de uma página web da marca fictícia **VESTE — Moda Consciente**:

* **Versão sem semântica**
* **Versão com HTML semântico**

O objetivo foi identificar problemas estruturais no código HTML sem semântica e aplicar soluções utilizando elementos semânticos, melhorando a acessibilidade, organização e interpretação da página por navegadores e tecnologias assistivas.

---

# Problemas Identificados e Soluções Aplicadas

## 1. Uso excessivo da tag `<div>`

### Problema

A estrutura da página utilizava `<div>` para praticamente todos os elementos.

Exemplo:

```html
<div class="topo">
<div class="conteudo">
<div class="rodape">
```

Isso dificulta a interpretação da estrutura da página.

### Solução

Substituição por tags semânticas específicas:

* `<header>`
* `<main>`
* `<section>`
* `<footer>`

### Benefício

Melhora a organização estrutural e facilita a leitura por navegadores e leitores de tela.

---

## 2. Ausência de hierarquia de títulos

### Problema

Os títulos foram criados usando `<div>` e `<span>`.

Exemplo:

```html
<div class="titulo-grande">
```

Esses elementos não possuem significado semântico.

### Solução

Substituição por:

* `<h1>`
* `<h2>`
* `<h3>`
* `<h4>`

### Benefício

Cria hierarquia correta de conteúdo e melhora navegação assistiva.

---

## 3. Menu de navegação sem semântica

### Problema

A navegação estava estruturada com `<div>`.

Exemplo:

```html
<div class="menu-links">
```

### Solução

Implementação com:

```html
<nav>
  <ul>
    <li>
```

### Benefício

Permite que tecnologias assistivas reconheçam a área como navegação principal.

---

## 4. Produtos sem estrutura independente

### Problema

Cada produto era representado apenas por `<div>`.

Exemplo:

```html
<div class="caixa-produto">
```

### Solução

Uso da tag:

```html
<article>
```

### Benefício

Define cada produto como conteúdo independente.

---

## 5. Lista de produtos sem estrutura de lista

### Problema

Os produtos estavam agrupados em uma `<div>`.

### Solução

Substituição por:

```html
<ul>
   <li>
```

### Benefício

Melhora a organização lógica do conteúdo.

---

## 6. Falta de acessibilidade

### Problema

Ausência de atributos que auxiliam leitores de tela.

### Solução

Adição de:

* `aria-label`
* `aria-labelledby`
* `aria-hidden`

Exemplo:

```html
<button aria-label="Buscar produtos">
```

### Benefício

Torna a página mais acessível para usuários com deficiência visual.

---

## 7. Rodapé sem identificação semântica

### Problema

O rodapé utilizava:

```html
<div class="rodape">
```

### Solução

Substituição por:

```html
<footer>
```

### Benefício

Identifica corretamente a área final da página.

---

# Resultados Obtidos

Após as correções, a página apresentou melhorias significativas:

* Melhor acessibilidade
* Melhor indexação por mecanismos de busca
* Estrutura mais organizada
* Código mais legível
* Melhor manutenção futura

---

# Conclusão

A versão sem semântica funcionava visualmente, porém apresentava limitações estruturais e de acessibilidade.

A aplicação de HTML semântico permitiu manter o mesmo layout visual, mas com uma estrutura correta, significativa e acessível, seguindo boas práticas do desenvolvimento web moderno.
