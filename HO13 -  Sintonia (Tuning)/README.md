Reescrever as consultas abaixo para maximizar a probabilidade delas serem executadas de maneira eficiente:

SELECT DISTINCT A.CPF, A.Nome <br>
FROM Funcionarios A <br>
WHERE A.CPF IN (SELECT CPF_Supervisor FROM Funcionarios) <br>
AND A.CPF NOT IN (SELECT CPF FROM Clientes) <br>
 

SELECT A.CodFilme, B.Nome <br>
FROM Midias A, Filmes B <br>
WHERE A.CodFilme = B.Codigo <br>
AND A.Tipo = "DVD" <br>
OR A.Tipo = "VHS" <br>
 

SELECT A.CPF_Cliente, A.ID_Midia, A.DataLocacao <br>
FROM Aluguel A, Clientes B <br>
WHERE A.CPF_Cliente = B.CPF <br>
AND B.Sexo != "F" <br>
AND EXISTS (SELECT * FROM Pagamentos C <br>
WHERE C.CPF_Cliente = A.CPF_Cliente <br>
AND C.ID_Midia = A.ID_Midia <br>
AND C.DataLocacao = A.DataLocacao) <br>
 

Considere o modelo relacional apresentado abaixo. Considere também que você não conhece os caminhos de acesso (índices) criados sobre os arquivos. 

![image](https://user-images.githubusercontent.com/89612369/210475147-479a920c-b105-4bd5-8380-5bb448cf0c53.png)
