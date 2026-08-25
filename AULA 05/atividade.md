## Atividade prática - Análise de Dados (Livraria) 📖
**Objetivo:**
- Crie um novo banco de dados para armazenar a tabela de livros
- Crie uma tabela com as colunas (id,nome,autor,preco,genero,
estoque,ano_publicacao)

![alt text](image.png)
![alt text](image-1.png)

---
## Bloco 1 — Reconhecimento da base 🎯
**Objetivo:** aprender a visualizar uma base de dados.

1- É exibido apenas os 10 primeiros dados da tabela:
```sql
SELECT * FROM livros LIMIT 10;
```
 ![alt text](image-2.png)

 ---
2- Como comprador só é interessante exibir as colunas nome, autor e preco de todos os livros:
```sql
SELECT nome, autor, preço FROM livros;
```
![alt text](image-3.png)

---
3- Em ordem afabetica é exibido a lista de generos distintos da livraria:
```sql
SELECT DISTINCT genero FROM livros ORDER BY genero;
```
![alt text](image-4.png)

---
4- Quantos autores há:
```sql
SELECT DISTINCT autor FROM livros;
```
![alt text](image-5.png)

---
5- Exibe os livros mais caros em uma ordem decrescente:
```sql
SELECT nome,preço FROM livros ORDER BY preço DESC LIMIT(5);
```
![alt text](image-7.png)

---
6- Exibe os livros com menor estoque para repor:
```sql
SELECT nome, estoque FROM livros ORDER BY estoque ASC LIMIT(5)
```
![alt text](image-6.png)

---
## Bloco 2 — Filtros numéricos 🔢
**Objetivo:** dominar os operadores de comparação e o BETWEEN.

7-Mostra o nome e estoque de todos os livros do gênero Técnico:
```sql
SELECT nome, estoque FROM livros WHERE genero = 'Técnico'
```
![alt text](image-8.png)

---
8- Exibe o nome e preço dos livros que custam mais de R$ 200,00:
```sql
SELECT nome,preço FROM livros WHERE preço > 200;
```
![alt text](image-9.png)

---
9- Mostra os livros que tem o preço entre 40 a 70 reais:
```sql
SELECT nome,preço FROM livros WHERE preço BETWEEN 40 AND 70;
```
![alt text](image-10.png)

---
10- Filtra o mostra os cinco livros com menores estoque para a livraria repor:
```sql
SELECT nome,estoque FROM livros WHERE estoque <5;
```
![alt text](image-11.png)

---
11-Livros publicados antes de 1900, ordenados do mais antigo para o mais recente.
```sql
SELECT nome,ano_publicacao FROM livros WHERE ano_publicacao <1900 ORDER BY ano_publicacao ASC;
```
![alt text](image-13.png)

---
12- Livros publicados entre 2010 e 2020, mostrando título, ano e gênero.
```sql
SELECT nome, ano_publicacao, genero FROM livros WHERE ano_publicacao BETWEEN 2010 AND 2020 ORDER BY ano_publicacao ASC;
```
![alt text](image-12.png)