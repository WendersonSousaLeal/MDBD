# MDBD — Modelagem de Banco de Dados

## Sobre o repositório

Este repositório reúne as atividades da disciplina de Modelagem de Banco de Dados, do curso técnico em Desenvolvimento de Sistemas (Etec, unidade São José dos Campos). As atividades vão desde exercícios de modelo lógico até o desenvolvimento completo do banco de dados `escola`.

## Estrutura do repositório

```
MDBD/
├── Atividade1 br_modelo/        # 10 exercícios de modelo lógico no brModelo (.brM3)
├── Atividade 2/                 # Diagrama, modelo e dump SQL iniciais do banco `escola`
├── Banco de Dados Escola/       # Evolução do banco `escola` (versões 1.0.0 e 1.0.1)
└── README.md
```

- **Atividade1 br_modelo/** — 10 modelos lógicos (`Lógico_1.brM3` a `Lógico_10.brM3`) criados na ferramenta brModelo.
- **Atividade 2/** — primeira versão do banco `escola`: diagrama em PDF (`Escola DATABASE.pdf`), arquivo de modelagem (`Escola.brM3`) e dump SQL (`escola.sql`).
- **Banco de Dados Escola/** — evolução do banco `escola`:
  - `escola.sql (1.0.0)` — versão inicial, com tabelas de associação extras (`alunos_cursos`, `alunos_turmas_cursos`) e diversas views de relatório.
  - `escola.sql (1.0.1)` — versão revisada, com a tabela `professores_disciplinas` consolidada e a adição do campo `status` (ativo/inativo) na tabela `alunos`.

## Tecnologias utilizadas

- brModelo (modelagem de dados lógica, arquivos `.brM3`)
- MySQL / MariaDB (scripts SQL exportados via phpMyAdmin)

## Como executar

- **Arquivos `.brM3`**: abrir no brModelo para visualizar ou editar os modelos.
- **Arquivos `.sql`**: importar via phpMyAdmin, ou executar `mysql -u root -p < escola.sql`, em um servidor MySQL/MariaDB (por exemplo, o do XAMPP).

## Observação

O banco `escola` criado e evoluído neste repositório é o mesmo consumido pelo projeto **App_Scholar** (React Native/Expo), por meio de uma API em PHP.

## Autor

Wenderson Sousa Leal
