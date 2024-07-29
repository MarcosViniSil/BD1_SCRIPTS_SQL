
/* CRIA TABELA ESCOLA */
CREATE TABLE Escola(
 codigo INT,
 nome VARCHAR(255),
 PRIMARY KEY(codigo)
);

/* CRIA TABELA PROJETO */

CREATE TABLE Projeto (
	codigo INT,
    nome VARCHAR(255),
    codEscola INT,
    PRIMARY KEY(codigo)
);

/* RELACIONA PROJETO COM ESCOLA */

ALTER TABLE Projeto ADD FOREIGN KEY (codEscola) REFERENCES Escola(codigo);

/* CRIA TABELA PROJETO */
CREATE TABLE ALUNO (
	codigo INT,
    nome VARCHAR(255),
    PRIMARY KEY(codigo)
);

/* CRIA TABELA PROJETO-ALUNO */
CREATE TABLE PROJETO_ALUNO (
	codProjeto INT,
    codAluno INT,
    cargaHoraria INT,
    PRIMARY KEY(codProjeto,codAluno) 
);

/* RELACIONA PROJETO_ALUNO COM PROJETO E ALUNO */

ALTER TABLE PROJETO_ALUNO ADD FOREIGN KEY (codProjeto) REFERENCES Projeto(codigo);
ALTER TABLE PROJETO_ALUNO ADD FOREIGN KEY (codAluno) REFERENCES ALUNO(codigo);

/* CRIA TABELA DISCIPLINA */
CREATE TABLE DISCIPLINA (
	cod INT,
    nome VARCHAR(255),
    PRIMARY KEY(cod)
);

/* CRIA TABELA DISCIPLINA */
CREATE TABLE DISCIPLINA_ALUNO (
	ano INT,
    codAluno INT,
    codDisciplina INT,
    nota FLOAT,
    PRIMARY KEY(ano)
);

/* RELACIONA PROJETO_ALUNO COM PROJETO E ALUNO */

ALTER TABLE DISCIPLINA_ALUNO ADD FOREIGN KEY (codAluno) REFERENCES ALUNO(codigo);
ALTER TABLE DISCIPLINA_ALUNO ADD FOREIGN KEY (codDisciplina) REFERENCES DISCIPLINA(cod);


select * from aluno;

/* REALIZA ALTERAÇÕES */

ALTER TABLE aluno ADD COLUMN dataNascimento DATE;
ALTER TABLE aluno ADD COLUMN sexo VARCHAR(1);


/* CRIA TABELA cidade */

CREATE TABLE cidade (
	codigo INT,
    nome INT,
    sigla INT
);
ALTER TABLE cidade
MODIFY COLUMN sigla VARCHAR(2);
ALTER TABLE cidade
MODIFY COLUMN nome VARCHAR(255);
/* ADICIONA CHAVE PRIMARIA EM CIDADE */

ALTER TABLE cidade ADD PRIMARY KEY (codigo) ;

/* ADICIONA codCidade EM ALUNO */

ALTER TABLE aluno ADD COLUMN codCidade INT;

/* RELACIONA codCidade EM ALUNO */

ALTER TABLE aluno ADD FOREIGN KEY (codCidade) REFERENCES cidade(codigo);

/* DELETA RELACIONAMENTO N -> N */
DROP TABLE projeto_aluno;

/* ADICIONA ALUNO EM PROJETO */
ALTER TABLE Projeto ADD COLUMN codAluno INT;

/* ADICIONA REFERENCIA ALUNO EM PROJETO */
ALTER TABLE Projeto ADD FOREIGN KEY (codAluno) REFERENCES ALUNO(codigo);

/* POVOANDO DADOS */

SELECT * FROM DISCIPLINA_ALUNO;

INSERT INTO Escola(codigo, nome) VALUES(1, "Escola1");
INSERT INTO Escola(codigo, nome) VALUES(2, "Escola2");
INSERT INTO Escola(codigo, nome) VALUES(3, "Escola3");
INSERT INTO Escola(codigo, nome) VALUES(4, "Escola4");

INSERT INTO DISCIPLINA(cod, nome) VALUES(1, "Disciplina1");
INSERT INTO DISCIPLINA(cod, nome) VALUES(2, "Disciplina2");
INSERT INTO DISCIPLINA(cod, nome) VALUES(3, "Disciplina3");
INSERT INTO DISCIPLINA(cod, nome) VALUES(4, "Disciplina4");

INSERT INTO cidade(codigo, nome,sigla) VALUES(5, "RIO DE JANEIRO","RJ");
INSERT INTO cidade(codigo, nome,sigla) VALUES(6, "SÃO PAULO","SP");
INSERT INTO cidade(codigo, nome,sigla) VALUES(7, "MINAS GERAIS","MG");
INSERT INTO cidade(codigo, nome,sigla) VALUES(8, "ESPIRITO SANTO","ES");

INSERT INTO ALUNO(codigo, nome,dataNascimento,sexo,codCidade) VALUES(1, "nome1","2024-01-01","M",1);
INSERT INTO ALUNO(codigo, nome,dataNascimento,sexo,codCidade) VALUES(2, "nome2","2024-01-01","F",2);
INSERT INTO ALUNO(codigo, nome,dataNascimento,sexo,codCidade) VALUES(3, "nome3","2024-01-01","F",2);
INSERT INTO ALUNO(codigo, nome,dataNascimento,sexo,codCidade) VALUES(4, "nome4","2024-01-01","M",3);

INSERT INTO PROJETO(codigo, nome,codEscola,codAluno) VALUES(1, "nome1",1,1);
INSERT INTO PROJETO(codigo, nome,codEscola,codAluno) VALUES(2, "nome2",1,2);
INSERT INTO PROJETO(codigo, nome,codEscola,codAluno) VALUES(3, "nome3",3,3);
INSERT INTO PROJETO(codigo, nome,codEscola,codAluno) VALUES(4, "nome4",2,4);

INSERT INTO DISCIPLINA_ALUNO(ano, codAluno,codDisciplina,nota) VALUES(2024, 1,1,7);
INSERT INTO DISCIPLINA_ALUNO(ano,codAluno,codDisciplina,nota) VALUES(2023, 2,2,8);
INSERT INTO DISCIPLINA_ALUNO(ano, codAluno,codDisciplina,nota) VALUES(2022, 3,3,5.9);
INSERT INTO DISCIPLINA_ALUNO(ano, codAluno,codDisciplina,nota) VALUES(2020, 4,4,7);





