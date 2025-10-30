**1.a) Selecione todas as colunas da tabela departamento. Repita o exercício para as tabelas funcionario, regiao e abrangencia**
-
## Respostas :



use treinamento;

select *
FROM departamento;

---------------------------------
use treinamento;

select *
FROM  funcionario;

-------
use treinamento;

select *
FROM  regiao;

----

use treinamento;

select *
FROM abrangencia;

----
**1.b) Selecione apenas as colunas cod_func, nome e cod_dept para a tabela funcionario**
-
Respostas
-
use treinamento;

select cod_func, nome, cod_dept
FROM funcionario;

-----
**2.a) Selecione todas as colunas da tabela funcionario que trabalham no departamento de código 30.**
-
Respostas
-

use treinamento;

select *
FROM Funcionario
Where cod_dept = "30";

---
**3.a) Liste todos os dados dos funcionários que não tenham gestores.**
-
Respostas
-
use treinamento;

select *
FROM  funcionario
WHERE cod_gestor IS NULL;
---
**4.a) Selecione o nome e código do departamento de todos os funcionários que trabalham no departamento >= 30 ou nao estejam alocados em nenhum departamento. 
**
-
use treinamento;

SELECT nome, cod_dept
FROM funcionario
WHERE cod_dept >= 30

---
**5.a) Liste o nome, cargo e salário de todos os funcionários, ordenado pelo salário, do maior para o menor.
**
-
use treinamento;

SELECT nome, cargo, salario
FROM funcionario
ORDER BY salario DESC

---
**6.a) Liste apenas o nome, cargo e salário para os 5 mais bem remunerados.
**
-
use treinamento;

SELECT nome, cargo, salario
FROM funcionario
ORDER BY salario DESC
LIMIT 10;

---
**7.a) Liste a quantidade de registros para a tabela departamento.
**
-
use treinamento;

SELECT COUNT(*)
FROM departamento

---
**7.b) Faça o mesmo do exercício anterior para as tabelas regiao, abrangencia e funcionario.
**
-
use treinamento;

SELECT COUNT(*)
FROM regiao, abrangencia, funcionario

---
**7.c) Liste a média de salário da empresa. 
**
-
use treinamento;

SELECT AVG (salario)
FROM funcionario

---
**7.d) Liste o código dos departamentos e quantidade de funcionários para cada departamento.
**
-
use treinamento;

SELECT cod_dept, COUNT(*)
from funcionario
GROUP BY cod_dept

---
**8.a) Liste o código dos departamentos e quantidade de funcionários para cada departamento, mas apenas para os departamentos com mais de 1 funcionário.
**
-
use treinamento;

SELECT cod_dept, COUNT(*)
from funcionario
GROUP BY cod_dept
HAVING COUNT(*)>1

