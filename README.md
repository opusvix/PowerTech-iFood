# Criar queries SQL com as cláusulas abaixo: 

- Recuperações simples com SELECT Statement
- Filtros com WHERE Statement
- Crie expressões para gerar atributos derivados
- Defina ordenações dos dados com ORDER BY
- Condições de filtros aos grupos – HAVING Statement
- Crie junções entre tabelas para fornecer uma perspectiva mais complexa dos dados

# Objetivo:
Refine o modelo apresentado acrescentando os seguintes pontos
- Cliente PJ e PF – Uma conta pode ser PJ ou PF, mas não pode ter as duas informações;
- Pagamento – Pode ter cadastrado mais de uma forma de pagamento;
- Entrega – Possui status e código de rastreio;
- Algumas das perguntas que pode fazer para embasar as queries SQL:
	- Quantos pedidos foram feitos por cada cliente?
	- Algum vendedor também é fornecedor?
	- Relação de produto e fornecedor
	- Relação de produto e estoque;
	- Relação de nomes dos fornecedores e nomes dos produtos;

# Perguntas adicionais a serem respondidas com as queries:
	- Qual o valor total das vendas com esses clientes? Deve conter: Nome do Cliente, Nome do produto, Quantidade Comprada, Preço unitário e total, Status do pedido, número da carteira digital e saldo da carteira digital. Ordenar por Status do pedido, nome do cliente e valor total da compra;
	- Quantos clientes cadastrados?
	- Quantos produtos cadastrados com preço maior que 500 reais?
	- Mostrar o nome e preço dos produtos com preço maior que 1000 reais
	- Relação do Nome do Cliente, CPF com o número da carteira digital
	- Relação do Nome do Cliente, CPF com o número da carteira digital de contas com saldo maior que 500 reais
	- Relação do Nome do Produto com a quantidade em estoque, retornando somente os que tem menos que 100 produtos em estoque para que seja feita reposição;
	- Qual o valor em reais de cada produto no estoque e o valor do estoque?
	- Qual o valor total em reais do estoque?
	- Qual a empresa responsável pela entrega em cada pedido, nome do cliente e endereço de entrega?
	

# Contextualizando o Modelo Lógico com base no Conceitual Construído

## Projeto de Banco de Dados de E-commerce

	- Contexto: Levantamento de requisitos
	- Projeto Conceitual: Modelo Entidade Relacionamento
	- Projeto Lógico: Modelo Relacional

## Modelando E-COMMERCE:
- Produto:
	- Os produtos são vendidos por uma única plataforma online. Contudo, estes podem ter vendedores distintos (terceiros)
	- Cada produto possui um fornecedor
	- Um ou mais produtos podem compor o pedido

- Cliente:
	- O cliente pode se cadastrar no site com seu CPF ou CNPJ
	- O endereço do cliente irá determinar o valor do frete
	- Um cliente pode comprar mais de um pedido. Este tem um período de carência para devolução do produto

- Pedido:
	- Os pedidos são criados por clientes e possuem informações de compra, endereço e status da entrega
	- Um produto ou mais compõem o pedido
	- O pedido pode ser cancelado

## Refinamento:
	- Cliente PJ e PF - Uma conta pode ser PJ ou PF, mas não pode ter as duas informações
	- Pagamento - Pode ter cadastrado mais de uma forma de pagamento
	- Entrega - possui status e código de rastreio
	- Foram adicionados itens a mais que julguei interessante para aproximar o projeto da realidade

### Software usado para modelagem
**MySQL Workbench**
