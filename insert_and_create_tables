/* CRIA TABELA LIVRO*/
CREATE TABLE Livro(
	codigo INT,
    descricao VARCHAR(255),
    ISBN INT,
    PRIMARY KEY(CODIGO)
);
/* CRIA TABELA EXEMPLAR*/
CREATE TABLE Exemplar(
	numero INT,
    situacao VARCHAR(255),
    codLivro INT,
    PRIMARY KEY(numero)
);
/* Adiciona cod livro em exemplar*/
ALTER TABLE Exemplar ADD FOREIGN KEY (codLivro) REFERENCES Livro(codigo);

/* CRIA TABELA Aluno*/
CREATE TABLE Aluno(
	codigo INT,
    nome VARCHAR(255),
    dataNascimento date,
    PRIMARY KEY(codigo)
);

/* CRIA TABELA Telefones*/
CREATE TABLE Telefone (
    telefone varchar(11),
    codAluno INT,
    PRIMARY KEY (telefone)
);

/* Adiciona cod aluno em telefone*/
ALTER TABLE Telefone ADD FOREIGN KEY (codAluno) REFERENCES Aluno(codigo);

/* CRIA TABELA Emprestimo*/
CREATE TABLE EMPRESTIMO (
    numexemplar INT,
    codaluno INT,
    dataretirada DATE,
    datadevolucao DATE,
    PRIMARY KEY(numexemplar,codaluno)

);

/* Adiciona aluno e exemplar à Emprestimo */

ALTER TABLE EMPRESTIMO ADD FOREIGN KEY (numexemplar) REFERENCES Exemplar(numero);
ALTER TABLE EMPRESTIMO ADD FOREIGN KEY (codaluno) REFERENCES Aluno(codigo);

/* POVOANDOO */

INSERT INTO ALUNO(codigo, nome, dataNascimento) VALUES(2, "Mesa", "2023-02-20");
INSERT INTO ALUNO(codigo, nome, dataNascimento) VALUES(3, "Mesa", "2023-02-20");
INSERT INTO ALUNO(codigo, nome, dataNascimento) VALUES(4, "Mesa", "2023-02-20");
INSERT INTO ALUNO(codigo, nome, dataNascimento) VALUES(5, "Mesa", "2023-02-20");

INSERT INTO livro(codigo, descricao, isbn) VALUES(1, "Mesa", 1);
INSERT INTO livro(codigo, descricao, isbn) VALUES(2, "Mesa", 1);
INSERT INTO livro(codigo, descricao, isbn) VALUES(3, "Mesa", 1);
INSERT INTO livro(codigo, descricao, isbn) VALUES(4, "Mesa", 1);

INSERT INTO exemplar(numero, situacao, codlivro) VALUES(1, "Mesa", 1);
INSERT INTO exemplar(numero, situacao, codlivro) VALUES(2, "Mesa", 1);
INSERT INTO exemplar(numero, situacao, codlivro) VALUES(3, "Mesa", 1);
INSERT INTO exemplar(numero, situacao, codlivro) VALUES(4, "Mesa", 1);

INSERT INTO emprestimo(numexemplar, codaluno, dataretirada,datadevolucao) VALUES(1, 1, "2023-02-20","2023-02-20");
INSERT INTO emprestimo(numexemplar, codaluno, dataretirada,datadevolucao) VALUES(2, 2, "2023-02-20","2023-02-20");
INSERT INTO emprestimo(numexemplar, codaluno, dataretirada,datadevolucao) VALUES(3, 3, "2023-02-20","2023-02-20");
INSERT INTO emprestimo(numexemplar, codaluno, dataretirada,datadevolucao) VALUES(4, 4, "2023-02-20","2023-02-20");

INSERT INTO telefone(telefone, codAluno) VALUES("31988957140", 1);
INSERT INTO telefone(telefone, codAluno) VALUES("31988957141", 2);
INSERT INTO telefone(telefone, codAluno) VALUES("31988957142", 3);
INSERT INTO telefone(telefone, codAluno) VALUES("31988957143", 4);