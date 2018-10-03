Desafio Hyperativa
==================

## Sobre o desafio

Tratamento e organização das informações de um sorteio.


### Exercício 01

Carregue a Base de Dados (base.sql) fornecida neste repositório e crie o relacionamento entre as tabelas do banco de dados.


### Exercício 02

Tabelas:

- Clientes - Cadastros de clientes
- Cartoes - Registros de cartão para um cliente (cadastro.Cliente)
- Transações - Registros de compra para um cartão (cartao.Cartao)
- NumerosDaSorte - Registros de números da sorte para cada cartão, gerados a partir das transações. (sorteio.NumerodaSorte)

Layout da tabela NumerosDaSorte:

- Codigo int
- CodigoTransacao int
- NumeroSorte bigint
- Criacao datetime

Para cada registro na tabela Transacoes (para um determinado cartão), precisamos criar 8 registros na tabela NumerosDaSorte, dentro do intervalo 
de data de 01/09/2012 até 25/11/2012. Caso existam registros fora desse intervalo, o cartão deverá ganhar o dobro de registros na tabela NumerosDaSorte. 
São válidas apenas transações com Valor igual ou acima de 10 reais.

Ex:

Cartao1 possui 20 transações no intervalo de data e 3 fora do intervalo. O mesmo deverá ganhar 160 registros referentes aos registros dentro do intervalo + 6 referentes as transações que estão fora do período, na tabela de NumerosDaSorte. Lembrando que são válidas apenas transações com Valor igual ou maior que 10 reais.

A coluna [NumeroSorte] da tabela NumerosDaSorte deve ser a soma do codigo do Cliente + codigo do Cartao + codigo da Transacao dividido por 3.

Crie uma Procedure para armazernar o script que você criou acima.


### Exercício 3:

Crie os indexs clustered e non-clustered se necessário, baseando-se nas consultas criadas por você. E explique de forma objetiva porque está criando os indexs.


### Exercício 4:

Para finalizar, crie uma view para preencher o modelo excel. O modelo pede o codigo do cliente e a quantidade de números da sorte por mês e ano.

# Boa Sorte

