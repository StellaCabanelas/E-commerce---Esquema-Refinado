# 📦 E-Commerce – Modelo Conceitual

Este repositório contém o **modelo conceitual** de um sistema de **E-Commerce**, representado através de um diagrama entidade-relacionamento (DER).  
O objetivo é fornecer a base para implementação de um banco de dados relacional que gerencie todo o fluxo de produtos, fornecedores, vendedores, clientes, pedidos, estoque e pagamentos.

## 🎯 Objetivo do Projeto
O esquema foi projetado para contemplar um cenário realista de comércio eletrônico, permitindo:

- Cadastro e gerenciamento de **produtos** e **estoque**.
- Relacionamento de **fornecedores** e **vendedores terceiros** com os produtos.
- Registro de **clientes** (pessoa física ou jurídica) e seus **pedidos**.
- Controle de **pagamentos** e **status dos pedidos**.
- Associação entre **produtos** e **pedidos**, com quantidades e descrições.

## 🗂 Estrutura do Modelo
O diagrama é composto por várias entidades principais:

- **Produto**: Item disponível para venda, podendo ser oferecido por fornecedores e vendedores terceiros.
- **Fornecedor**: Empresa responsável por disponibilizar produtos no sistema.
- **Terceiro – Vendedor**: Vendedor externo (marketplace) que também pode ofertar produtos.
- **Cliente**: Comprador, podendo ser pessoa física ou jurídica.
- **Pedido**: Registro de compra realizado pelo cliente, com status e descrição.
- **Pagamento**: Registro de transações financeiras associadas aos clientes.
- **Estoque**: Locais e quantidades disponíveis de cada produto.
- **Relacionamentos**: Tabelas auxiliares para ligação entre produtos, pedidos, vendedores, fornecedores e estoque.

## 🔗 Principais Relacionamentos
- **Fornecedor → Produto**: Através da tabela `Disponibilizando um produto`.
- **Vendedor Terceiro → Produto**: Através da tabela `Produtos por Vendedor`.
- **Produto → Estoque**: Controlado pela tabela `Produto_has_Estoque`.
- **Produto → Pedido**: Associado pela tabela `Relação de Produto/Pedido`.
- **Cliente → Pedido**: Um cliente pode ter vários pedidos.
- **Cliente → Pagamento**: Um cliente pode ter múltiplos registros de pagamento.
- **Cliente → Pessoa Física/Jurídica**: Permite identificar o tipo de cliente.

## 📌 Benefícios do Modelo
- Suporte a múltiplos fornecedores e vendedores.
- Controle detalhado de estoque por localidade.
- Flexibilidade para atender clientes de diferentes naturezas.
- Histórico de pedidos e pagamentos rastreável.
- Estrutura escalável para futuras funcionalidades, como promoções e avaliações.

## 📷 Diagrama
<img width="860" height="1058" alt="Image" src="https://github.com/user-attachments/assets/3177e403-e835-4e61-bb8f-c995fcd9a898" />
