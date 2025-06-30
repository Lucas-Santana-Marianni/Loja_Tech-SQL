# 🕹️ Loja Gamer - Banco de Dados

Este projeto representa um banco de dados simples para gerenciamento de produtos em uma loja voltada ao público gamer.

## 📁 Banco de Dados: `lojaTech`

### 🧾 Tabela: `Produtos`

A tabela `Produtos` armazena os itens disponíveis na loja.

| Campo       | Tipo             | Descrição                    |
|-------------|------------------|------------------------------|
| id_loja     | INT (PK)         | Identificador do produto     |
| nome        | VARCHAR(100)     | Nome do produto              |
| preco       | DECIMAL(10,2)    | Preço do produto             |
| estoque     | INT              | Quantidade em estoque        |

### 📦 Inserts iniciais

```sql
insert into Produtos (nome, preco, estoque) values
('Notebook', 3500.00, 10),
('Mouse', 50.00, 200),
('Teclado', 120.00, 150),
('Monitor', 800.00, 30),
('Cadeira Gamer', 1500.00, 5);

🔍 Consultas SQL disponíveis:

select * from Produtos;

select nome, preco from Produtos;

select nome, preco from Produtos where preco > 1000;

select nome, estoque from Produtos where estoque >= 30;

select nome, preco from Produtos order by preco asc;

select nome, preco from Produtos where nome like 'M%';

select * from Produtos where estoque between 10 and 100;

select * from Produtos where nome not in ('Mouse', 'Teclado');

select * from Produtos where nome like '%Gamer%';

select * from Produtos where preco = (select max(preco) from Produtos);
