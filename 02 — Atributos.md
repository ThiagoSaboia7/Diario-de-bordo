# Atributos

## 1. Conceito

Atributos são as **características que descrevem cada entidade dentro do domínio**.

Por exemplo, um cliente possui:

```text
+-----------------------+
|        CLIENTE        |
+-----------------------+
| Nome                  |
| Endereço              |
| Telefone              |
+-----------------------+
```

Durante a análise de requisitos, são identificados os atributos importantes de cada entidade naquele contexto, de forma a manter o modelo o mais simples possível e consequentemente armazenar apenas as informações que serão úteis futuramente.

Uma pessoa possui atributos pessoais como cor dos olhos, altura e peso, mas para um sistema que funcionará em um supermercado, estas informações dificilmente serão relevantes.

---

## 2. Classificação quanto à função

Os atributos podem ser classificados quanto à sua função da seguinte forma:

```text
                    ATRIBUTOS
                        |
          +-------------+-------------+
          |             |             |
          v             v             v
     DESCRITIVOS    NOMINATIVOS   REFERENCIAIS
```

### 2.1 Descritivos

> Representam característica essenciais de uma entidade, tais como nome ou cor.

```text
Exemplos:

+-----------------------+
|      DESCRITIVOS      |
+-----------------------+
| Nome                  |
| Cor                   |
+-----------------------+
```

---

### 2.2 Nominativos

> Além de serem também descritivos, estes têm a função de definir e identificar um objeto.

Nome, código, número são exemplos de atributos nominativos.

```text
Exemplos:

+-----------------------+
|      NOMINATIVOS      |
+-----------------------+
| Nome                  |
| Código                |
| Número                |
+-----------------------+
```

---

### 2.3 Referenciais

> Representam a ligação de uma entidade com outra em um relacionamento.

Por exemplo, uma venda possui o CPF do cliente, que a relaciona com a entidade cliente.

```text
+------------------+                +------------------+
|     CLIENTE      |                |      VENDA       |
+------------------+                +------------------+
| CPF              | -------------> | CPF do cliente   |
+------------------+                +------------------+
```

---

## 3. Classificação quanto à estrutura

Quanto à sua estrutura, podemos ainda classificá-los como:

```text
                  ATRIBUTOS
                      |
              +-------+-------+
              |               |
              v               v
           SIMPLES         COMPOSTOS
```

### 3.1 Simples

> Um único atributo define uma característica da entidade.

Exemplos: nome, peso.

```text
+-----------------------+
|        PESSOA         |
+-----------------------+
| Nome                  |
| Peso                  |
+-----------------------+
```

---

### 3.2 Compostos

> Para definir uma informação da entidade, são usados vários atributos.

Por exemplo, o endereço pode ser composto por rua, número, bairro, etc.

```text
                 ENDEREÇO
                    |
        +-----------+-----------+
        |           |           |
        v           v           v
       RUA        NÚMERO      BAIRRO
```

---

## 4. Chave Primária

Alguns atributos representam valores únicos que identificam a entidade dentro do domínio e não podem se repetir.

Em um cadastro de clientes, por exemplo, esse atributo poderia ser o CPF.

A estes chamamos de **Chave Primária**.

```text
+--------------------------------+
|            CLIENTE             |
+--------------------------------+
| [PK] CPF                       |
|      Nome                      |
|      Endereço                  |
|      Telefone                  |
+--------------------------------+

PK = Chave Primária
```

---

## Estrutura Geral

```text
+==================================================+
|                    ATRIBUTOS                     |
+==================================================+
                         |
            +------------+------------+
            |                         |
            v                         v
          FUNÇÃO                   ESTRUTURA
            |                         |
    +-------+-------+          +------+------+
    |       |       |          |             |
    v       v       v          v             v
Descrit. Nominat. Referenc.  Simples       Compostos


                IDENTIFICAÇÃO ÚNICA
                        |
                        v
                 CHAVE PRIMÁRIA
```

---

## Referência

**DevMedia — MER e DER: Modelagem de Bancos de Dados**

