# Introdução à Modelagem de Dados

## Introdução

O primeiro passo para o desenvolvimento de uma aplicação de sistema é o levantamento dos requisitos necessários, para a edificação do produto final.

Durante essa análise, identifica-se as principais partes e objetos envolvidos, suas possíveis ações e responsabilidades, suas características e como elas interagem entre si.

Com os resultados obtidos você poderá criar um modelo conceitual que se consiste em uma visão de alto nível e abstrata que organiza os conceitos as informações e as regras de um sistema.

---

## Modelo Entidade Relacionamento (MER)

Utilizado para descrever os objetos (entidades) envolvidos em um domínio de negócios, como sua características (atributos) e como elas se relacionam.

### Estrutura do MER

```text
ENTIDADES
   │
   ├── ATRIBUTOS
   │
   └── RELACIONAMENTOS
```

---

## Entidades

Entidades são nomeadas com substantivos concretos ou abstratos que representem de forma clara sua função dentro do domínio, que podem ser classificados como físicos ou lógicos.

### Entidades Físicas

Cliente, pessoa, empresa, ou um produto: carro, computador.

### Entidades Lógicas

Exige interação com Entidade Física como um cliente realizar uma compra.

---

## Classificação das Entidades

Podemos classificar as entidades segundo o motivo de sua existência:

### Entidades Fortes

São aquelas cuja existência independe de outras entidades, ou seja, por si só elas já possuem total sentido de existir.

Como um site de vendas conter produtos.

```text
SITE DE VENDAS
      │
      └── PRODUTOS
```

---

### Entidades Fracas

São aquelas que dependem de outras entidades para existirem.

Como a entidade venda depende da entidade produto.

```text
PRODUTO
   │
   └── VENDA
```

---

### Entidades Associativas

São aquelas que surge quando há a necessidade de associar uma entidade a um relacionamento existente.

Na modelagem Entidade-Relacionamento não é possível que um relacionamento seja associado a uma entidade, então tornamos esse relacionamento uma entidade associativa, que a partir daí poderá se relacionar com outras entidades.

### Exemplo

Quando duas pessoa se casam, o que prova que elas estão juntas é a certidão de casamento.

```text
PESSOA ───── CASAMENTO ───── PESSOA
                  │
                  ↓
        CERTIDÃO DE CASAMENTO
```

O conceito de Entidade Associativa é exatamente esse:

> Ela é o "papel" que registra quando duas coisas do mundo real interagem, se conectam ou realizam uma transação.

---

## Referência

DevMedia — MER e DER: Modelagem de Bancos de Dados

