Apresentar a árvore de consulta inicial (não otimizada) com o parsing da consulta em ordem natural (da esquerda para a direita), a árvore de consulta inicial (não otimizada) com o parsing da consulta em ordem reversa (da direita para a esquerda), a árvore de consulta otimizada, a consulta reescrita de acordo com a árvore de consulta otimizada com o parsing da consulta em ordem natural (da esquerda para a direita), a consulta reescrita de acordo com a árvore de consulta otimizada com o parsing da consulta em ordem reversa (da direita para a esquerda) e o plano de execução da consulta otimizada para cada uma das consultas SQL apresentadas abaixo:

SELECT A.CPF, A.Nome, B.Nome <br>
FROM Funcionarios A, Clientes B, Aluguel C, Funcionarios D<br>
WHERE A.CPF=B.CPF<br>
AND B.CPF=C.CPF_Cliente<br>
AND B.Sexo="M"<br>
AND C.ValorPagar>50<br>
AND A.CPF=D.CPF_Supervisor<br>


SELECT A.Nome, C.Nome<br>
FROM Filmes A, AtoresEmFilmes B, Atores C, Midias D<br>
WHERE A.Codigo=B.CodFilme<br>
AND B.CodAtor=C.Codigo<br>
AND A.Genero="Aventura"<br>
AND A.Codigo=D.CodFilme<br>
AND D.PrecoDiaria>10<br>
 

SELECT A.CPF, A.Nome, B.Nome<br>
FROM Funcionarios A, Clientes B, Aluguel C, Pagamentos D  <br>
WHERE A.CPF=B.CPF  <br>
AND C.ValorPagar>100  <br>
AND B.CPF=C.CPF_Cliente  <br>
AND D.Valor<50  <br>
AND A.CPF_Supervisor IS NULL  <br>
AND A.CPF=C.CPF_Funcionario <br>


Considere o modelo relacional apresentado abaixo, e que todos os arquivos são ISAM com índices secundários em suas chaves estrangeiras. 

![image](https://user-images.githubusercontent.com/89612369/210474955-2c9e4931-ba1b-42c3-9e1c-7c674968ed3b.png)


Considere também que o ponteiro para blocos de disco tem 16B, que o tamanho de bloco de disco é de 2KB, que os arquivos possuem registros de tamanho fixo, não espalhados e que eles têm a seguinte configuração de número de registros e tamanhos de campos: 
<ul>
<li> Atores (10.000 registros) → Codigo (16B), Nome (160B)
<li> Clientes (100.000 registros) → CPF (11B), Nome (160B), Endereco (200B), Telefone (16B), DataNascimento (12B), Sexo (1B)
<li> Filmes (2.000.000 registros) → Codigo (16B), Nome (160B), Genero (80B)
<li> Funcionarios (3.500 registros) → CPF (11B), Nome (160B)
<li> Midias (10.000.000 registros) → Identificador (24B), Tipo (8B), PrecoDiaria (24B)
<li> Aluguel (20.000.000 registros)  → DataLocacao (12B), DataDevolucao (10B), ValorPagar (24B)
<li> Pagamentos (50.000.000 registros) → Codigo (48B), Data (12B), Valor (24B)
<li> AtoresEmFilmes (1.000.000 registros)
Observem a existência de chaves estrangeiras que obviamente devem ser consideradas como campos integrantes dos arquivos.
