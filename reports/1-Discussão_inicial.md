# Introdução

Conforme solicitado no e-mail referente a etapa inicial do projeto, verificou-se as informações.

## 1. Verificação de inconsistências

### 1.1. Valores nulos:
Através da colsulta verificou-se a existência de valores nulos na coluna 'curso'

SELECT * FROM `aluno` WHERE `curso` IS NULL;
![alt text](image-1.png)

### 1.2. Cursos fora do especificado

A tabela deve conter informações sobre os seguintes cursos:

- Informática
- Psicologia
- Comunicação

SELECT * FROM `aluno` WHERE `curso` NOT IN ('Informática', 'Psicologia', 'Comunicação');
![alt text](image.png)

### 1.3.Verificação das médias de entrada e saída

Médias de entrada fora do range

SELECT * FROM `aluno` WHERE `media_entrada`< 10 OR `media_entrada` >20;
![alt text](image-2.png)


Alunos que conluíram o curso com notas fora do range

SELECT * FROM `aluno` WHERE` media_final`< 10 OR `media_final` >20;
![alt text](image-3.png)

Alunos que concluiram o curso e não tem a média final

SELECT * FROM `aluno` WHERE `media_final` IS NULL AND `curso_concluido` = 1;

![alt text](image-4.png)


## 2. Verificação das relações entre média de entrada e média final

Verificando a correlação entre as variáveis, observou-se um fenômeno inconsistente:
![alt text](image-5.png)

A correlação calculada indica que as médias se comportam de forma inversamente proporcionais, ou seja, quanto maior a nota de entrada, menor a nota de saída e vice-versa. Faz sentido?