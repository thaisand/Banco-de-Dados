Construir um índice multinível estático na chave primária e índices multinível dinâmicos com árvore B+ em cada chave estrangeira para cada arquivo (tabela) presente no modelo relacional abaixo, apresentando a blocagem (fator de bloco), o número de blocos necessários para armazenar o índice, o espaço total gasto para armazenar cada arquivo de índice e o número de acessos a blocos necessários para recuperar um registro usando cada índice construído.

![image](https://user-images.githubusercontent.com/89612369/210474696-0fab1972-2d7e-4972-9c91-191fbc9a8ed7.png)


Considere que o ponteiro para blocos de disco tem 16B, que o tamanho de bloco de disco é de 2KB, que um nó de árvore B+ seja armazenado em um bloco de disco, que a ocupação na árvore B+ seja de 69%, que cada ponteiro de nó da árvore B+ ocupe 12B, que os arquivos possuem registros de tamanho fixo, não espalhados e que eles têm a seguinte configuração de número de registros e tamanhos de campos:
<ul>
<li> Atores (10.000 registros) → Codigo (16B), Nome (160B)
<li> Clientes (100.000 registros) → CPF (11B), Nome (160B), Endereco (200B), Telefone (16B), DataNascimento (12B), Sexo (1B)
<li> Filmes (2.000.000 registros) → Codigo (16B), Nome (160B), Genero (80B)
<li> Funcionarios (3.500 registros) → CPF (11B), Nome (160B)
<li> Midias (10.000.000 registros) → Identificador (24B), Tipo (8B), PrecoDiaria (24B)
<li> Aluguel (20.000.000 registros)  → DataLocacao (12B), DataDevolucao (10B), ValorPagar (24B)
<li> Pagamentos (50.000.000 registros) → Codigo (48B), Data (12B), Valor (24B)
<li> AtoresEmFilmes (1.000.000 registros)
<li> Observem a existência de chaves estrangeiras que obviamente devem ser consideradas como campos integrantes dos arquivos.
