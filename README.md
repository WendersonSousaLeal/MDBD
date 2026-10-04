# MDBD — Modelagem de Banco de Dados

## Sobre o projeto

Repositório que reúne a modelagem e o desenvolvimento de bancos de dados relacionais criados na disciplina de Modelagem de Banco de Dados do curso técnico em Desenvolvimento de Sistemas (Etec São José dos Campos).

O principal resultado é o banco de dados `escola`, que gerencia informações acadêmicas como alunos, cursos, turmas, professores e disciplinas. O repositório contém o diagrama, os modelos lógicos, os scripts SQL e o dicionário de dados do banco, além de exercícios de modelagem feitos no brModelo.

O banco `escola` é o mesmo utilizado pelo aplicativo **App_Scholar** (React Native/Expo), que o acessa por meio de uma API em PHP. O código do aplicativo está no repositório [PROGRAMACAO-MOBILE](https://github.com/WendersonSousaLeal/PROGRAMACAO-MOBILE).

## Funcionalidades

- Modelagem lógica de bancos de dados no brModelo (10 exercícios)
- Diagrama e modelo do banco `escola`
- Scripts SQL para criação das tabelas do banco `escola`
- Tabelas de associação para relacionamentos muitos-para-muitos (`alunos_cursos`, `alunos_turmas_cursos`, `professores_disciplinas`)
- Views de relatório na versão 1.0.0 do banco
- Controle de situação do aluno (ativo/inativo) pelo campo `status`, na versão 1.0.1
- Dicionário de dados com campos, restrições, chaves e finalidade de cada tabela

## Tecnologias utilizadas

- brModelo
- MySQL / MariaDB
- phpMyAdmin
- Git
- GitHub

## Estrutura do projeto

```
MDBD/
├── Atividade1 br_modelo/                      # 10 exercícios de modelo lógico (.brM3)
├── Atividade 2/                               # Primeira versão do banco `escola`
├── Banco de Dados Escola/                     # Evolução do banco `escola` (1.0.0 e 1.0.1)
├── Dicionario de Dados/                       # Dicionário de dados (PDF)
└── README.md
```

- **Atividade1 br_modelo/**: modelos lógicos `Lógico_1.brM3` a `Lógico_10.brM3`.
- **Atividade 2/**: diagrama (`Escola DATABASE.pdf`), modelo (`Escola.brM3`) e dump SQL (`escola.sql`) iniciais.
- **Banco de Dados Escola/**: modelo atualizado (`Escola.brM3`) e as versões do script SQL:
  - `1.0.0`: versão inicial, com tabelas de associação extras e views de relatório.
  - `1.0.1`: versão revisada, com a tabela `professores_disciplinas` consolidada e o campo `status` (`CHAR(1)`, padrão `'A'`) na tabela `alunos`.
- **Dicionario de Dados/**: `Dicionario_de_Dados_App_Scholar.pdf`, que documenta o banco `escola`.

## Requisitos

- MySQL ou MariaDB (por exemplo, o servidor do XAMPP)
- brModelo (para abrir os arquivos `.brM3`)
- Git

## Como executar

1. Clone o repositório:
   ```
   git clone https://github.com/WendersonSousaLeal/MDBD.git
   ```
2. Acesse a pasta do projeto:
   ```
   cd MDBD
   ```
3. Para visualizar ou editar os modelos, abra os arquivos `.brM3` no brModelo.
4. Para criar o banco, inicie o servidor MySQL/MariaDB e importe o script SQL mais recente (versão `1.0.1`, na pasta `Banco de Dados Escola`) pelo phpMyAdmin ou pelo terminal:
   ```
   mysql -u root -p < escola.sql
   ```

## Autor

Wenderson Sousa Leal
