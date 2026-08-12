# Relacionamentos

## 1. Relacionamentos

Com as Entidades identificadas podemos classifica-las de três formas:

```text
+==================================================+
|                 RELACIONAMENTOS                  |
+==================================================+
                        |
          +-------------+-------------+
          |             |             |
          v             v             v
         1..1          1..N          N..N
      UM PRA UM    UM PARA MUITOS  MUITOS PARA
                                    MUITOS
```

---

## 2. Relacionamento 1..1 — Um pra Um

> Cada uma das duas entidades envolvidas referenciam obrigatoriamente apenas uma unidade da outra.

Por exemplo uma pessoa possui apenas um cpf e um número de cpf pertence a apenas uma pessoa.

### Representação

```text
+------------------+             +------------------+
|      PESSOA      |             |       CPF        |
+------------------+             +------------------+
         |                              |
         |           1 .. 1             |
         +------------------------------+
```

```text
PESSOA  1  <-------------------->  1  CPF
```

---

## 3. Relacionamento 1..N — Um para Muitos

> Uma das entidades envolvidas pode referenciar várias unidades da outra, porém, do outro lado cada uma das várias unidades referenciadas só pode estar ligada uma unidade da outra entidade.

Por exemplo uma mãe pode ter vários filhos mas um filho possui apenas uma mãe.

### Representação

```text
+------------------+             +------------------+
|       MÃE        |             |      FILHO       |
+------------------+             +------------------+
         |                              |
         |           1 .. N             |
         +------------------------------+
```

```text
MÃE  1  <----------------------->  N  FILHO
```

---

## 4. Relacionamento N..N — Muitos para Muitos

> Neste tipo de relacionamento cada entidade, de ambos os lados, podem referenciar múltiplas unidades da outra.

Por exemplo um ator atua em vários filmes e um filme possui vários atores.

### Representação

```text
+------------------+             +------------------+
|       ATOR       |             |      FILME       |
+------------------+             +------------------+
         |                              |
         |           N .. N             |
         +------------------------------+
```

```text
ATOR  N  <----------------------->  N  FILME
```

---

## 5. Estrutura dos Relacionamentos

```text
+==================================================+
|                 RELACIONAMENTOS                  |
+==================================================+
                        |
       +----------------+----------------+
       |                |                |
       v                v                v
     1 .. 1           1 .. N           N .. N
       |                |                |
       v                v                v
   UM PRA UM       UM PARA MUITOS    MUITOS PARA
                                       MUITOS
       |                |                |
       v                v                v
 PESSOA -- CPF      MÃE -- FILHO      ATOR -- FILME
```

---

## Referência

**DevMedia — MER e DER: Modelagem de Bancos de Dados**
