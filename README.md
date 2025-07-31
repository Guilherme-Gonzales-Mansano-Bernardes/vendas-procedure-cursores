# vendas-procedure-cursores
Projeto MySQL que demonstra o uso de cursores dentro de procedures para processar vendas de vendedores. Cria tabelas, insere dados e calcula total e média das vendas, armazenando os resultados em outra tabela. Excelente para aprender manipulação avançada e controle de fluxo em SQL.

## Passo 1: Criação do banco e da tabela

STEP 1
Criamos o banco de dados com o comando CREATE DATABASE CURSORES; para armazenar o projeto.
Selecionamos o banco usando USE CURSORES; para garantir que os próximos comandos sejam executados nele.
Criamos a tabela VENDEDORES, que guarda o nome do vendedor e as vendas dos meses de janeiro, fevereiro e março. O campo IDVENDEDOR é a chave primária com auto incremento para identificar unicamente cada vendedor.

STEP 2
Inserimos os dados dos vendedores na tabela usando o comando INSERT INTO VENDEDORES VALUES, adicionando os nomes e as vendas dos meses de janeiro, fevereiro e março.
O valor NULL no primeiro campo indica que o IDVENDEDOR será gerado automaticamente pelo auto incremento.

STEP 3
Criamos a tabela VEND_TOTAL para armazenar os dados dos vendedores junto com o cálculo do total e da média das vendas.
A estrutura inclui o nome do vendedor, vendas dos meses de janeiro, fevereiro e março, além das colunas para o total e a média das vendas, usando o comando CREATE TABLE VEND_TOTAL.

STEP 4
Antes de criar a procedure, alteramos o delimitador padrão com DELIMITER $, que é essencial para que o banco consiga interpretar corretamente o bloco de comandos da procedure, já que ela contém múltiplas instruções separadas por ponto e vírgula.
Em seguida, criamos a procedure INSEREDADOS, que usa um cursor para percorrer a tabela VENDEDORES, calcular o total e a média das vendas de janeiro, fevereiro e março, e inserir esses valores na tabela VEND_TOTAL.
O uso do cursor, o tratamento do fim da leitura com DECLARE CONTINUE HANDLER, o loop REPEAT...UNTIL e os comandos FETCH e INSERT INTO fazem parte da lógica para processar e salvar os dados de forma automatizada.
Por fim, a procedure fecha o cursor para liberar recursos.

STEP 5
Após criar a procedure, restauramos o delimitador padrão com o comando DELIMITER ; para que os comandos normais possam ser executados normalmente.
Em seguida, executamos a procedure com o comando CALL INSEREDADOS();, que processa os dados da tabela VENDEDORES e insere os resultados na tabela VEND_TOTAL.

RESUMO:
Procedures com cursores são úteis quando precisamos:

Percorrer registros linha a linha dentro do banco de dados.

Fazer cálculos, somas ou médias de campos de forma automática.

Alimentar tabelas de relatórios ou resultados consolidados sem depender de código externo.

É muito usado em sistemas de ERP, relatórios gerenciais e rotinas de atualização de dados.

----------------

Para desenvolver essa query e procedure, é importante ter:

Conhecimento intermediário de SQL (criar tabelas, inserir dados, consultar).

Entender a estrutura de uma procedure no MySQL.

Saber como funciona um cursor para percorrer registros.

Conhecimento básico de controle de fluxo no SQL, como REPEAT...UNTIL, DECLARE HANDLER e variáveis locais.
