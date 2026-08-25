## Parte 01
**Criação e inserção de dados, realizando consultas avançadas.**

```sql
CREATE TABLE produtos(
    id SERIAL PRIMARY KEY,
    nome VARCHAR(60) NOT NULL,
    valor DECIMAL(10,2) NOT NULL,
    categoria VARCHAR(30) NOT NULL,
    estoque INTEGER NOT NULL
)
```
---
```sql
INSERT INTO produtos (nome, categoria, valor, estoque) VALUES
```
---
Seleciona apenas os 5 primeiros id para mostras na tabela:
```sql
SELECT * FROM produtos LIMIT 5;
```
---
Mostra apenas os citados:
```sql
SELECT nome, valor,categoria FROM produtos;
```
---
Mostra as categorias separadas:
```sql
SELECT DISTINCT categoria FROM produtos ORDER BY categoria;
```
## Parte 02
Filtro de dados.

Para filtras produtos por categoria:
```sql
 SELECT nome, estoque FROM produtos WHERE categoria = 'Monitores'
 ```
---
Filtro de valor:
```sql
SELECT nome,estoque FROM produtos WHERE valor > 1000;
```
---
Filtro entre faixar de valores:
```sql
SELECT nome,estoque FROM produtos WHERE valor BETWEEN 100 AND 500;
```
---
Busca por trecho de texto:
```sql
SELECT nome,estoque FROM produtos WHERE nome LIKE 'Mouse%'
```