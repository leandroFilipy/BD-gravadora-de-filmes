# 💽 Scripts SQL – Banco de Dados para Diversos Cenários

Este projeto contém a criação e manipulação de tabelas em bancos de dados SQL, abrangendo cenários como uma gravadora de filmes, instituições de ensino e sistemas hospitalares. Os comandos demonstram a prática de **DDL** (Data Definition Language) e **DML** (Data Manipulation Language) em MySQL.

---

## 📁 Estrutura Geral

```sql
-- Banco: GRAVADORA_FILMES
CREATE DATABASE gravadora_filmes;
USE gravadora_filmes;

CREATE TABLE filmes (
  id_filme INT,
  nome_filme VARCHAR(50),
  genero_filme VARCHAR(50),
  classificaçao_etaria VARCHAR(50)
);

CREATE TABLE atores (
  id_ator INT,
  nome_ator VARCHAR(50),
  estado_civil_ator VARCHAR(50),
  data_nascimento_ator DATE
);

CREATE TABLE orcamento (
  id_orcamento INT,
  orcamento_do_filme VARCHAR(50)
);

CREATE TABLE sala_de_efeitos_visuais (
  id_cena INT,
  sala VARCHAR(50),
  tempo_estimado VARCHAR(50)
);

CREATE TABLE sala_mixagem_de_som (
  id_mixagem INT,
  funcionario VARCHAR(50),
  tempo_estimado VARCHAR(50)
);

CREATE TABLE equipe_de_limpeza (
  id_funcionario INT,
  materias_utilizados VARCHAR(50)
);

CREATE TABLE estudio_de_gravação (
  id_sala_degravação INT,
  bloco VARCHAR(50),
  sala VARCHAR(50)
);

CREATE TABLE diretor_de_fotografia (
  id_diretor INT,
  nome_diretor VARCHAR(50),
  data_nascimento_diretor DATE
);

ALTER TABLE diretor_de_fotografia ADD estado_civil VARCHAR(50);
ALTER TABLE diretor_de_fotografia ADD salario_diretor_de_fotografia VARCHAR(50) AFTER data_nascimento_diretor;

ALTER TABLE filmes ADD duração_filme VARCHAR(50);
ALTER TABLE filmes CHANGE id_filme id_filmess INT;
ALTER TABLE filmes MODIFY duração_filme VARCHAR(60);
ALTER TABLE filmes RENAME TO filmess;
ALTER TABLE filmess RENAME TO filmes;
ALTER TABLE filmes DROP duração_filme;
