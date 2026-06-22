# Achei! - Achados e Perdidos

## 1. Contexto do Problema e Solução

### O Problema é:

Em um campus universitário é muito comum que alunos, funcionários e moradores percam pertences. Fones de ouvido, cartão do onibus/RU, chaves, celulares e outros itens. Sem um canal centralizado o processo de recuperação fica desorganizado e mais difícil: avisos informais em grupos de WhatsApp, posts nos Stories do Instagram e dependência da boa vontade de quem encontrou o item. Isso resulta em itens esquecidos em mesas de secretaria, portarias e cantinas sem nenhum registro formal, tornando a devolução ao dono praticamente impossível.

### A solução é:

O **Achei!** é um sistema web que centraliza o processo de registro e devolução de itens no campus. Com ele:

- **Quem perde** um item pode cadastrá-lo no sistema com descrição, categoria e situação, facilitando a busca.
- **Quem encontra** pode entregar o item a um posto de apoio, onde um funcionário irá registrar o item e informar em qual posto de apoio (Cantina, Biblioteca, Portaria Central etc.) ele foi entregue.
- **A retirada** é formalizada com um Termo de Retirada registrando o CPF e email do retirante, garantindo fidelidade na devolução.
- **Gestores** podem cadastrar e gerenciar os postos de apoio disponíveis no campus.

O sistema requer login de usuário (alunos, funcionários, etc) e oferece operações completas de cadastro, consulta, edição e exclusão (CRUD) tanto para os postos de apoio quanto para o registro completo de devolução de itens.

---

## 2. Instruções para Uso do Git

## 2.1. Estrutura de Pastas do Projeto

O repositório deverá seguir a seguinte organização:

```txt
/
├── Documentação/          # Documentação do projeto
│   ├── Requisitos/        # Documento de requisitos, casos de uso e regras de negócio
│   ├── Padrões Adotados/         
│
├── src/                   # Código-fonte da aplicação
│   ├── backend/           # Código do backend
│   ├── frontend/          # Código do frontend
│   └── database/          # Scripts de banco de dados
│
├── tests/                 # Testes do sistema
│
├── README.md              # Descrição geral do projeto
└── .gitignore             # Arquivos e pastas ignorados pelo Git
```

## 2.2. Regras de Branches

Para evitar conflitos e facilitar o desenvolvimento em equipe, o projeto utilizará branches com finalidades específicas.

### Branch principal

```txt
main
```

A branch `main` deve conter apenas versões estáveis do projeto. Nenhuma alteração deve ser enviada diretamente para ela sem revisão.

### Branch de desenvolvimento

```txt
develop
```

A branch `develop` será usada para integrar as funcionalidades em desenvolvimento antes de enviá-las para a branch principal.


O fluxo de trabalho do grupo será:

Criar ou escolher uma issue relacionada à tarefa que será feita.
Atualizar a branch develop antes de começar a alteração.
Desenvolver a funcionalidade, correção ou documentação necessária.
Realizar commits pequenos e objetivos, seguindo o padrão definido.
Enviar as alterações para a branch develop.
Quando a versão estiver funcionando, integrar a branch develop na branch main.
Manter a branch main apenas com versões estáveis do projeto.

Dessa forma, o grupo consegue trabalhar de maneira mais simples, utilizando a develop como branch de desenvolvimento geral e a main como branch final do projeto.

## 2.3. Padrão de Commits

As mensagens de commit devem seguir um padrão semântico, inspirado no modelo de commits convencionais. Esse padrão facilita a leitura do histórico e ajuda a entender rapidamente o tipo de alteração realizada.

Formato:

```txt
tipo: descrição breve da alteração
```

Exemplos:

```txt
feat: adiciona cadastro de item perdido
fix: corrige erro ao realizar login
docs: atualiza documento de requisitos
style: ajusta formatação do código
refactor: reorganiza classes de usuário
test: adiciona testes para cadastro de posto
chore: atualiza configurações do projeto
```

## Tipos de Commit

Os principais tipos de commit utilizados serão:

| Tipo     | Uso                                               |
| -------- | ------------------------------------------------- |
| feat     | Adição de nova funcionalidade                     |
| fix      | Correção de erro                                  |
| docs     | Alterações na documentação                        |
| style    | Ajustes de formatação, sem alterar funcionamento  |
| refactor | Refatoração de código                             |
| test     | Criação ou alteração de testes                    |
| chore    | Configurações, dependências ou tarefas auxiliares |

## Boas Práticas de Commit

Os commits devem ser pequenos, claros e relacionados a uma única alteração.

Evitar mensagens vagas como:

```txt
alterações
atualização
arrumando coisas
commit final
```

Preferir mensagens específicas como:

```txt
feat: cria tela de cadastro de posto de apoio
docs: adiciona diagrama de classes
fix: corrige validação de campos obrigatórios
```

## 2.4. Uso de Issues

Cada tarefa do projeto deverá ser registrada como uma issue no GitHub. As issues devem possuir título claro, descrição objetiva e, quando possível, estar associadas ao quadro Kanban do projeto.

Exemplos de issues:

```txt
RF010 - Cadastrar Item Perdido (Backend)
RF010 - Cadastrar Item Perdido (Frontend)
RF010 - Criar tabela Item Perdido no banco de dados
RF020 - Gerenciar Postos de Apoio
```

## 2.5. Pull Requests

As alterações devem ser enviadas por meio de Pull Requests. Antes de aprovar um Pull Request, o grupo deverá verificar:

* se o código está funcionando;
* se não há conflitos;
* se o padrão de commits foi seguido;
* se a documentação foi atualizada quando necessário;
* se a tarefa está vinculada à issue correspondente.


## 2.6. Arquivo .gitignore

O arquivo `.gitignore` será usado para impedir que arquivos desnecessários sejam enviados ao repositório, como arquivos temporários, arquivos de configuração local, caches e dependências geradas automaticamente.


---

## 3. Instruções para Devs

> Será preenchido durante o desenvolvimento!

---

## 4. Tecnologias

### Frontend

| Tecnologia | Versão | Finalidade |
|---|---|---|
| HTML | 5 (W3C Living Standard) | Estrutura das páginas web |
| CSS | 3 (W3C Living Standard) | Estilização e layout responsivo |
| JavaScript | ES2025 (ECMAScript 16) | Interatividade |

### Backend

| Tecnologia | Versão | Finalidade |
|---|---|---|
| Python | 3.13.13 | Linguagem de programação principal |
| Flask | 3.1.3 | Framework web: rotas, templates, requisições HTTP |
| SQLAlchemy | 2.0.43 | ORM — mapeamento objeto-relacional com o banco de dados |

### Banco de Dados

| Tecnologia | Versão | Finalidade |
|---|---|---|
| SQLite | 3.53.2 | Banco de dados em desenvolvimento (arquivo local, sem servidor) |
| PostgreSQL | 18.4 | Banco de dados em produção / apresentação |

### Outras

| Tecnologia | Versão | Finalidade |
|---|---|---|
| VS Code | 1.123 | IDE de desenvolvimento |
| Git | 2.x | Controle de versão |
| GitHub | — | Hospedagem do repositório e colaboração entre membros |

---

## 5. Organização do Projeto

> Será preenchido durante o desenvolvimento!

---

## 6. Equipe

* Christian Miguel Lopes
* José Geraldo Caria da Silva
* Pedro Henrique Gonçalves Reis
