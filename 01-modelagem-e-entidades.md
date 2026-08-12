# Introdução à Modelagem de Dados 

> **Objetivo:** Apresentar os conceitos iniciais de Modelagem de Dados, Modelo Entidade-Relacionamento (MER) e classificação das entidades.

---

## 1. Introdução

O primeiro passo para o desenvolvimento de uma aplicação de sistema é o levantamento dos requisitos necessários, para a edificação do produto final.

Durante essa análise, identifica-se as **principais partes e objetos envolvidos**, suas possíveis **ações e responsabilidades**, suas **características** e como elas **interagem entre si**.

Com os resultados obtidos você poderá criar um **modelo conceitual** que se consiste em uma visão de alto nível e abstrata que organiza os conceitos as informações e as regras de um sistema.

```text
LEVANTAMENTO DE REQUISITOS
           |
           v
  ANÁLISE DOS OBJETOS
           |
           v
   MODELO CONCEITUAL
```

---

## 2. Modelo Entidade Relacionamento (MER)

Utilizado para descrever os **objetos (entidades)** envolvidos em um domínio de negócios, como sua **características (atributos)** e como elas **se relacionam**.

### Estrutura do MER

```text
+--------------------------------------------------+
|         MODELO ENTIDADE RELACIONAMENTO           |
+--------------------------------------------------+
                       |
          +------------+------------+
          |            |            |
          v            v            v
      ENTIDADES    ATRIBUTOS   RELACIONAMENTOS
```

---

## 3. Entidades

Entidades são nomeadas com substantivos concretos ou abstratos que representem de forma clara sua função dentro do domínio, que podem ser classificados como **físicos ou lógicos**.

### 3.1 Entidades Físicas

Cliente, pessoa, empresa, ou um produto: carro, computador.

```text
+-----------------------+
|   ENTIDADES FÍSICAS   |
+-----------------------+
| Cliente               |
| Pessoa                |
| Empresa               |
| Carro                 |
| Computador            |
+-----------------------+
```

### 3.2 Entidades Lógicas

Exige interação com Entidade Física como um cliente realizar uma compra.

```text
+---------+       realiza       +--------+
| CLIENTE | ------------------> | COMPRA |
+---------+                      +--------+
```

---

## 4. Classificação das Entidades

Podemos classificar as entidades segundo o motivo de sua existência:

```text
                    ENTIDADES
                        |
          +-------------+-------------+
          |             |             |
          v             v             v
       FORTES         FRACAS      ASSOCIATIVAS
```

---

### 4.1 Entidades Fortes

> **São aquelas cuja existência independe de outras entidades, ou seja, por si só elas já possuem total sentido de existir.**

Como um site de vendas conter produtos.

```text
+------------------+
|  SITE DE VENDAS  |
+------------------+
         |
         v
+------------------+
|     PRODUTOS     |
+------------------+
```

---

### 4.2 Entidades Fracas

> **São aquelas que dependem de outras entidades para existirem.**

Como a entidade venda depende da entidade produto.

```text
+------------------+
|     PRODUTO      |
+------------------+
         |
         | depende
         v
+------------------+
|      VENDA       |
+------------------+
```

---

### 4.3 Entidades Associativas

> **São aquelas que surge quando há a necessidade de associar uma entidade a um relacionamento existente.**

Na modelagem Entidade-Relacionamento não é possível que um relacionamento seja associado a uma entidade, então tornamos esse relacionamento uma **entidade associativa**, que a partir daí poderá se relacionar com outras entidades.

#### Exemplo

Quando duas pessoa se casam, o que prova que elas estão juntas é a certidão de casamento.

```text
+----------+                      +----------+
| PESSOA A | ------ CASAMENTO ---| PESSOA B |
+----------+          |           +----------+
                      |
                      v
            +---------------------+
            |      CERTIDÃO       |
            |    DE CASAMENTO     |
            +---------------------+
```

O conceito de Entidade Associativa é exatamente esse:

> Ela é o **"papel"** que registra quando duas coisas do mundo real interagem, se conectam ou realizam uma transação.

---

## 5. Visão Geral

```text
+==================================================+
|               MODELAGEM DE DADOS                |
+==================================================+
                       |
                       v
            LEVANTAMENTO DE REQUISITOS
                       |
                       v
                MODELO CONCEITUAL
                       |
                       v
                      MER
                       |
          +------------+------------+
          |            |            |
          v            v            v
      ENTIDADES    ATRIBUTOS   RELACIONAMENTOS
          |
          +------------+------------+
          |            |            |
          v            v            v
       FORTES         FRACAS      ASSOCIATIVAS
```

---

## Referência

**DevMedia — MER e DER: Modelagem de Bancos de Dados**
