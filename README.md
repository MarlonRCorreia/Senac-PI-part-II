# 💻 Projeto Integrador III: Desenvolvimento de Sistemas Orientado a Objetos (2ª Entrega)

## 👤 Integrantes do Grupo 49
* [cite_start]Anna Caroline Moreira Picanço [cite: 569]
* [cite_start]Denyzard Ubirajara Larios Moreira [cite: 570]
* [cite_start]Marlon Rogério Correia Santana [cite: 571]
* [cite_start]Matheus Nunes Friedrich [cite: 572]
* [cite_start]Thiago Barbosa Silva [cite: 573]

---

## 1. Modelagem UML (Fase 1)

### 1.1. Diagrama de Casos de Uso
O diagrama representa as interações no **Sistema de Cadastro**.

* **Atores Principais (Pessoa Física):** Professor e Aluno.
* **Atores Principais (Pessoa Jurídica):** Fornecedor.

| Caso de Uso | Atores | Ações Chave |
| :--- | :--- | :--- |
| Criar Login | Pessoa Física, Professor, Aluno | [cite_start]Inclui: Validar CPF e dados cadastrais. [cite: 574] [cite_start]Estende: Exibir erro dados inválidos. [cite: 574] |
| Fazer Login | Pessoa Física, Professor, Aluno | [cite_start]Inclui: Validar Login. [cite: 574] [cite_start]Estende: Exibir usuário ou senha inválidos. [cite: 574] |
| Cadastrar Fornecedor | Pessoa Jurídica, Fornecedor | [cite_start]Inclui: Validar CNPJ. [cite: 574] [cite_start]Estende: Exibir CNPJ inválido e Realizar Cotação. [cite: 574] |

### 1.2. Diagrama de Classes
[cite_start]As classes foram modeladas com base no princípio da Herança. [cite: 736]

| Classe | Herda de | Atributos Principais | Métodos Principais |
| :--- | :--- | :--- | :--- |
| **Pessoa Física** | [cite_start]Nenhuma | nome, cpf, dataNascimento, telefone, endereço, email [cite: 739] [cite_start]| cadastrar(), login() [cite: 740] |
| **Professor** | [cite_start]Pessoa Física [cite: 741] [cite_start]| disciplina [cite: 742] [cite_start]| atribuirNota() [cite: 743] |
| **Aluno** | [cite_start]Pessoa Física [cite: 744] [cite_start]| disciplina, nota, media [cite: 745] [cite_start]| calcularNota() [cite: 746] |
| **Pessoa Jurídica** | [cite_start]Nenhuma (Associação com PF no diagrama) | cnpj, razaoSocial, cnae [cite: 748] [cite_start]| realizarCotacao() [cite: 749] |
| **Fornecedor** | [cite_start]Pessoa Jurídica [cite: 750] [cite_start]| idFornecedor [cite: 751] [cite_start]| receberPedido() [cite: 752] |

---

## 2. Protótipos de Interface (Fase 2 - Entrega 1)

Os protótipos das interfaces foram desenvolvidos para refletir os casos de uso de cadastro, utilizando [Miro/Figma - **MUDAR AQUI**].

As telas desenvolvidas cobrem as seguintes jornadas:

* Cadastro de Pessoa Física
* Cadastro de Pessoa Jurídica
* Cadastro de Professores
* Cadastro de Fornecedores
* Cadastro de Alunos


## 3. Modelo de Dados e Scripts SQL (Fase 2 - Entrega 2)

Os scripts DDL e DML necessários para o armazenamento dos dados modelados estão disponíveis na pasta `/scripts_sql`.

### 3.1. DDL (Data Definition Language)

**Scripts DDL disponíveis em: `/scripts_sql/DDL.sql`**

* Criação das tabelas `PessoaFisica`, `Aluno`, `Professor`, `PessoaJuridica` e `Fornecedor`.
* Definição de chaves primárias e estrangeiras para garantir a integridade referencial.

### 3.2. DML (Data Manipulation Language)

**Scripts DML disponíveis em: `/scripts_sql/DML.sql`**

* Comandos `INSERT` de exemplo para popular todas as tabelas.
* Exemplos de consultas (`SELECT`) podem ser adicionados para demonstração.

```markdown
**COLOQUE AQUI OS SEUS SCRIPTS SQL DDL E DML para facilitar a visualização.**
