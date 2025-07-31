# vendas-procedure-cursores
Projeto MySQL que demonstra o uso de cursores dentro de procedures para processar vendas de vendedores. Cria tabelas, insere dados e calcula total e média das vendas, armazenando os resultados em outra tabela. Excelente para aprender manipulação avançada e controle de fluxo em SQL.

## Passo 1: Criação do banco e da tabela

![Criação do banco e tabela](C:\Users\Guilherme Dev\Desktop\gith/Steap1.png)

Legenda:  
Criamos o banco de dados com o comando **CREATE DATABASE CURSORES;** para armazenar o projeto.  
Selecionamos o banco usando **USE CURSORES;** para garantir que os próximos comandos sejam executados nele.  
Criamos a tabela **VENDEDORES**, que guarda o nome do vendedor e as vendas dos meses de janeiro, fevereiro e março. O campo **IDVENDEDOR** é a chave primária com auto incremento para identificar unicamente cada vendedor.
