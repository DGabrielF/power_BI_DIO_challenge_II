# power_BI_DIO_challenge_II
About Este repositório tem como finalidade armazenar o relatório desenvolvido durante o curso de Power BI do Bootcamp Python Data Analytics

## Descrição da resolução
1. Transferir os dados para o Power BI
2. Iniciar a Transformação de dados
employee:
* remoção das linhas com ssn == null (3. ✅)
* transformando ssn, ssn.super e department.number em texto (1. ✅)
* transformando salary em número decimal fixo  (2. ✅)
* separando a coluna address pelo primeiro "-" para obter o address.number (8. ✅)
* separando a coluna address pelo último "-" para obter o address.state (8. ✅)
* separando a coluna address pelo último "-" para obter o address.city e adress.street (8. ✅)
* como em nenhum momento o estado mudou a coluna de estado foi removida (15. ✅)
* como não possuímos a rua e o número do endereço dos departamentos, não faz sentido continuar carregando a rua e o número do endereço dos empregados nesta análise (15. ✅)
* mesclando as tabelas employee com department e verificando onde cada funcionário trabalha (9. ✅)
* mesclando a coluna de nomes dos funcionários (12. ✅)
* conectando os ssn.super com o ssn para obter o nome do gerente de cara funcionário (11. ✅)
* renomeando colunas (name, ssn, birthdate, city, gender, salary, ssn.super, department.number) (1. ✅)
department:
* transformando department.number e ssn.super em texto (1. ✅)
* renomeando colunas (department.name, department.number, ssn.super, super.start_date, department.create_date) (1. ✅)
dependent:
* transformando ssn em texto (1. ✅)
* renomeando colunas (ssn, dependent.name, gender, birthdate, relationship) (1. ✅)
dept_location:
* transformando department.number em texto (1. ✅)
* mesclando a tabela de localização com a tabela de departamentos
* Criando uma coluna para abstrair o nome do departamento com a cidade, criando uma identificação única
* renomeando colunas (department.number, city) (1. ✅)
project:
* transformando project.number e department.number em texto (1. ✅)
* transformando "." (pontos) em "," (vírgulas) para evitar a conversão de números em datas (7. ✅)
* renomeando colunas (project.name, project.number, city, department) (1. ✅)
work_on:
* remoção das linhas com ssn == null  (3. ✅)
* transformando ssn e project_number em texto (1. ✅)
* renomeando colunas (ssn, project.number, hours)  (1. ✅)

## Lista de requisitos do desafio
1. Verifique os cabeçalhos e tipos de dados ✅
2. Modifique os valores monetários para o tipo double preciso✅
3. Verifique a existência dos nulos e analise a remoção✅
4. Os employees com nulos em Super_ssn podem ser os gerentes. Verifique se há algum colaborador sem gerente✅
  - O único sem ssn.super é o Borg, que é gerente do Headquarter e dos gerentes Jennifer e Franklin
5. Verifique se há algum departamento sem gerente✅
  - Todos os departamentos possuem gerentes.
6. Se houver departamento sem gerente, suponha que você possui os dados e preencha as lacunas✅
7. Verifique o número de horas dos projetos✅
8. Separar colunas complexas✅
9. Mesclar consultas employee e departament para criar uma tabela employee com o nome dos departamentos associados aos colaboradores. A mescla terá como base a tabela employee. Fique atento, essa informação influencia no tipo de junção✅
10. Neste processo elimine as colunas desnecessárias.✅
11. Realize a junção dos colaboradores e respectivos nomes dos gerentes . Isso pode ser feito com consulta SQL ou pela mescla de tabelas com Power BI. Caso utilize SQL, especifique no README a query utilizada no processo. ✅
12. Mescle as colunas de Nome e Sobrenome para ter apenas uma coluna definindo os nomes dos colaboradores✅
13. Mescle os nomes de departamentos e localização. Isso fará que cada combinação departamento-local seja único. Isso irá auxiliar na criação do modelo estrela em um módulo futuro.✅
14. Agrupe os dados a fim de saber quantos colaboradores existem por gerente✅
15. Elimine as colunas desnecessárias, que não serão usadas no relatório, de cada tabela✅
