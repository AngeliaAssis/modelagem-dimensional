
# ⭐ Modelagem Dimensional - Star Schema

Projeto do desafio de modelagem dimensional do Bootcamp Engenharia de Dados - NTT DATA da [DIO](https://www.dio.me/).


## Objetivo do projeto
1. Criar o diagrama dimensional – star schema – com base no diagrama relacional disponibilizado.

2. O diagrama dimensional deverá conter a tabela 'Fato' relacionada ao contexto analisado (tabela 'Professor') e as tabelas 'Dimensão' que serão compostas pelos detalhes relacionados ao contexto.

3. Adição de uma tabela dimensão de datas.


## Etapas do projeto
Visando consolidar todo o conteúdo de processamento de dados e modelagem, o projeto foi criado com as seguintes etapas:
1. Replicar o diagrama relacional no [SqlDBM](https://sqldbm.com/Home/).
2. Geração de SQL no SqlDBM para gerar o script de criação do banco de dados.
3. Criação do novo banco de dados MySQL na instância do Azure.
4. Criação das tabelas.
5. Conexão do banco de dados MySQL com o Power BI.
6. Fazer a modelagem dos dados no Power BI com o Power Query.
7. Criar o diagrama dimensional - star schema.


## Aplicações utilizadas
[SqlDBM](https://sqldbm.com/Home/)<br>
Banco de dados MySQL no Azure<br>
Cloud Shell Azure<br>
Power BI<br>
Power Query<br>


## Fases da modelagem de dados
1. Verificar como o Power BI reconhece a modelagem e relacionamentos.

2. Fazer transformações no Power Query:

a. renomear as tabelas

b. remoção das colunas geradas pelo Power BI decorrente do relacionamento identificado (nome_banco_de_dados.nome_coluna).

c. verificar se 'tipo de dado' está de acordo com a modelagem relacional.

d. tabela 'professor' considerada como objeto de análise.

e. 'mesclar consultas em nova tabela' entre a tabela 'professor' e a tabela 'departamento' na coluna de junção 'idDepartamento'. Criada a tabela fato 'f_professor'. Colunas expandidas 'nome departamento' e 'campus departamento'

f. 'mesclar consultas na mesma tabela' entre a tabela 'f_professor' e as tabelas 'disciplina&curso' e 'curso'.

g. criação da tabela 'data' com as colunas 'idCurso', 'carga horária', 'duração', data de início'.

h. 'mesclar consultas na mesma tabela' entre a tabela 'f_professor' e a tabela 'data' na coluna de junção 'idCurso'. Coluna expandida 'carga horária'.

i. tabelas excluídas: 'aluno', 'matriculado', 'pré-requisitos', 'pré-requisitos das disciplinas' e 'disciplina'.


3. Criação das relações através do Power BI em 'gerenciar relações'. Modelagem dimensional em star schema concluída.



