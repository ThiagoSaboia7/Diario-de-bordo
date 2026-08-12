# MER e DER

## 1. Modelo Entidade-Relacionamento — MER

O MER é um **modelo conceitual** que tem como objetivo representar a estrutura e a organização das informações que serão armazenadas em um banco de dados.

Por meio dele, são identificadas as principais **entidades**, seus **atributos** e os **relacionamentos** existentes entre essas entidades.

Por exemplo, em um sistema de uma loja, podemos ter as entidades Cliente, Produto e Venda, cada uma possuindo seus próprios atributos e relacionamentos.

### Representação

```text
+==================================================+
|                       MER                        |
|               MODELO CONCEITUAL                  |
+==================================================+
                         |
            +------------+------------+
            |            |            |
            v            v            v
        ENTIDADES     ATRIBUTOS   RELACIONAMENTOS
            |
      +-----+-----+
      |     |     |
      v     v     v
 CLIENTE PRODUTO VENDA
```

---

## 2. Diagrama Entidade-Relacionamento — DER

O DER é a **representação visual e gráfica** do modelo definido pelo MER.

Ele utiliza elementos gráficos para facilitar a compreensão da estrutura do banco de dados.

Normalmente, as entidades são representadas por **retângulos**, os atributos são apresentados associados às entidades e os relacionamentos são representados por **linhas ou outras formas**, dependendo da notação utilizada.

Além disso, o DER pode apresentar as **cardinalidades**, que indicam quantas ocorrências de uma entidade podem estar relacionadas a outra, como, por exemplo, um cliente poder realizar várias compras.

### Representação

```text
+------------------+          +------------------+
|     CLIENTE      |          |      VENDA       |
+------------------+          +------------------+
| CPF              |          | Código           |
| Nome             |          | Data             |
+------------------+          +------------------+
         |                            |
         |           1 .. N           |
         +----------------------------+
```

---

## 3. MER x DER

```text
+==================================================+
|                    MER x DER                     |
+==================================================+

              +-------------------+
              |        MER        |
              +-------------------+
                       |
                       v
              MODELO CONCEITUAL
                       |
                       v
         Estrutura e organização
              das informações
                       |
                       v
        Entidades + Atributos +
             Relacionamentos
                       |
                       |
                       v
              +-------------------+
              |        DER        |
              +-------------------+
                       |
                       v
           REPRESENTAÇÃO VISUAL
                E GRÁFICA
                       |
                       v
          Representa visualmente
           o modelo definido
               pelo MER
```

### Diferença principal

| MER                                                  | DER                                                                          |
| ---------------------------------------------------- | ---------------------------------------------------------------------------- |
| Modelo conceitual                                    | Representação visual e gráfica                                               |
| Representa a estrutura e organização das informações | Representa graficamente o modelo definido pelo MER                           |
| Identifica entidades, atributos e relacionamentos    | Apresenta visualmente entidades, atributos, relacionamentos e cardinalidades |

---

## Referência

**DevMedia — MER e DER: Modelagem de Bancos de Dados**
