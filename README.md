# SQL_BANCO_DE_DADOS_ESCOLA-2
CREATE DATABASE escola;
USE escola;

DROP TABLE IF EXISTS escola;
CREATE TABLE escola (
    id INT NOT NULL,
    nome VARCHAR(80) NOT NULL,
    portugues NUMERIC(3,1) NOT NULL,
    matematica NUMERIC(3,1) NOT NULL,
    fisica NUMERIC(3,1) NOT NULL,
    historia NUMERIC(3,1) NOT NULL,
    CONSTRAINT pk_escola PRIMARY KEY (id)
);

INSERT INTO escola (id, nome, portugues, matematica, fisica, historia) VALUES
(1, 'Tony Stark', 4.0, 10.0, 10.0, 1.0),
(2, 'Zé Colméia', 0.0, 2.5, 0.0, 3.0),
(3, 'Carlisle Cullen', 10.0, 10.0, 10.0, 10.0),
(4, 'Batman', 0.0, 10.0, 10.0, 8.0),
(5, 'Penélope Charmosa', 0.0, 5.0, 8.0, 7.0),
(6, 'Viúva Negra', 10.0, 7.0, 7.0, 10.0);

SELECT * FROM escola;
SELECT nome, portugues, matematica FROM escola ORDER BY nome;
SELECT * FROM escola WHERE id = 3;
SELECT * FROM escola WHERE nome = 'Carlisle Cullen';
SELECT * FROM escola WHERE nome LIKE '%cullen%';
SELECT * FROM escolaalunoalunoalunoalunodiciplina WHERE nome LIKE '%cullen';
SELECT * FROM escola WHERE nome LIKE 'cullen%';

SELECT * FROM escola WHERE matematica > 5;
SELECT * FROM escola WHERE portugues >= 6;
SELECT nome, portugues FROM escola WHERE portugues >= 6;
SELECT * FROM escola WHERE matematica >= 5 AND fisica >= 8;

SELECT nome, matematica, fisica
FROM escola
WHERE matematica >= 5 AND fisica >= 8
ORDER BY nome;

SELECT * FROM escola WHERE portugues >= 5 OR historia >= 5;
SELECT * 
FROM escola
WHERE portugues >= 5 OR historia >= 5
ORDER BY nome;
