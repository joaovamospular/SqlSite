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
