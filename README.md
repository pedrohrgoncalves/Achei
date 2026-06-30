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

# 2. Instruções para Uso do Git

## 2.1. Estrutura de Pastas do Projeto

O repositório deverá seguir a seguinte organização:

```txt
/
├── Documentação/          # Documentação do projeto
│   ├── Requisitos/        # Documento de requisitos, casos de uso e regras de negócio
│   ├── Padrões Adotados/         
│
├── Achei!/                # Código-fonte da aplicação
│   ├── app/               # Código do backend e criação e configuração do banco de dados
│   ├── frontend/          # Código do frontend
│   └── scripts/           # Scripts de banco de dados
│   └── tests/             # Testar requisições do sistema
│                
├── achei.db
├── requirements.txt
├── README.md
```
### Pastas e arquivos internos estão detalhados na sessão 5: Organização do Projeto

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

# 3. Instruções para Devs

## Boas Práticas de Codificação

Para garantir a legibilidade, organização e manutenção do código, o grupo deverá seguir as seguintes boas práticas durante o desenvolvimento do sistema.

### 3.1. Indentar corretamente o código

A indentação será usada para organizar visualmente o código e deixar claros os blocos de comandos, como estruturas `if`, `else`, `while`, `for`, funções e classes.

Um código bem indentado facilita a leitura, ajuda a identificar o escopo de cada instrução e reduz a chance de erros durante a manutenção.

Exemplo:

```python
if usuario_logado:
    listar_itens_perdidos()
else:
    exibir_tela_login()
```

### 3.2. Nomear variáveis de maneira intuitiva

As variáveis deverão possuir nomes claros e relacionados ao seu significado dentro do sistema. O grupo deverá evitar nomes genéricos ou sem sentido, como `x`, `y`, `a1` ou `array1`, quando eles não representarem bem a informação armazenada.

Exemplo inadequado:

```python
x = "Pedro"
```

Exemplo adequado:

```python
nome_usuario = "Pedro"
```

Essa prática facilita o entendimento do código por qualquer integrante do grupo.

### 3.3. Evitar condições negativas desnecessárias no `if`

Sempre que possível, as condições deverão ser escritas de forma positiva, verificando primeiro a situação verdadeira e deixando a situação alternativa para o `else`.

Isso torna o código mais direto e evita confusão, principalmente em estruturas condicionais maiores ou aninhadas.

Exemplo menos legível:

```python
if not usuario_ativo:
    bloquear_acesso()
else:
    liberar_acesso()
```

Exemplo mais legível:

```python
if usuario_ativo:
    liberar_acesso()
else:
    bloquear_acesso()
```

### 3.4. Nomear funções de maneira intuitiva

As funções deverão ter nomes que indiquem claramente a ação realizada. O nome da função deve ajudar a entender sua finalidade sem que seja necessário analisar todo o seu conteúdo.

Exemplos:

```python
cadastrar_item_perdido()
listar_postos_apoio()
validar_email()
gerar_termo_retirada()
```

Funções que retornam valores booleanos também deverão ter nomes claros, indicando uma verificação.

Exemplos:

```python
email_valido()
usuario_ativo()
item_disponivel()
```

### 3.5. Comentar e documentar o código quando necessário

O código deverá conter comentários em trechos importantes, principalmente quando houver regras de negócio, validações ou lógicas mais complexas.

Comentários não devem ser usados para explicar comandos óbvios, mas sim para esclarecer a intenção de uma regra ou funcionamento.

Exemplo adequado:

```python
# Verifica se o item já foi retirado antes de permitir nova retirada
if item.retirado:
    return "Item indisponível"
```

Além dos comentários, nomes claros de variáveis, funções e classes também serão usados como forma de tornar o código mais autoexplicativo.

### 3.6. Padronizar nomes de constantes

As constantes deverão seguir um padrão de nomenclatura para serem facilmente identificadas no código. O grupo adotará nomes em letras maiúsculas, separando palavras com underline.

Exemplos:

```python
MAX_TENTATIVAS_LOGIN = 3
STATUS_ITEM_DISPONIVEL = "disponivel"
STATUS_ITEM_RETIRADO = "retirado"
```

Essa prática ajuda a diferenciar valores fixos de variáveis comuns, facilitando a leitura e a manutenção do sistema.

---
# 4. Tecnologias

## Frontend

| Tecnologia | Versão | Finalidade |
|---|---:|---|
| HTML | Living Standard | Estrutura das páginas web. |
| CSS | CSS Snapshot 2026 | Estilização, tema visual em azul suave, responsividade e organização dos elementos da interface. |
| JavaScript | ECMAScript 2026 | Interatividade do sistema, controle de login, permissões de tela e chamadas `fetch()` para o backend. |

## Backend

| Tecnologia | Versão | Finalidade |
|---|---:|---|
| Python | 3.14.x | Linguagem principal do backend. |
| FastAPI | 0.121.3 | Framework web usado para criar a API, rotas HTTP, validação de dados e documentação automática em `/docs`. |
| Uvicorn | 0.38.0 | Servidor ASGI utilizado para executar a aplicação FastAPI localmente. |
| Pydantic | 2.x | Biblioteca utilizada para validação dos dados enviados nas requisições da API. |

## Banco de Dados

| Tecnologia | Versão | Finalidade |
|---|---:|---|
| SQLite | 3.x | Banco de dados local utilizado no desenvolvimento. O banco é salvo em arquivo, geralmente `achei.db`, sem necessidade de servidor externo. |
| sqlite3 | Módulo padrão do Python | Biblioteca usada pelo backend para conectar, criar tabelas e executar consultas SQL no SQLite. |

## Outras Ferramentas

| Tecnologia | Versão | Finalidade |
|---|---:|---|
| VS Code | 1.120 | IDE/editor utilizado no desenvolvimento do projeto. |
| Git | 2.x | Controle de versão do código-fonte. |
| GitHub | — | Hospedagem do repositório e colaboração entre membros. |
| Pytest | 9.0.1 | Execução dos testes automatizados do backend. |
| HTTPX | 0.28.1 | Cliente HTTP usado nos testes automatizados da API. |

---
# 5. Organização do Projeto


O projeto **Achei!** está estruturado para garantir uma separação clara entre a interface do usuário, a lógica de servidor, os testes automatizados e os arquivos auxiliares.

A organização geral do projeto segue o modelo abaixo:

```text
Achei/
├── app/
│   ├── __init__.py
│   ├── main.py
│   ├── db.py
│   └── schemas.py
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   ├── script.js
│   └── README_FRONTEND.md
│
├── tests/
│   └── test_crud.py
│
├── scripts/
│   └── exemplo_requisicoes.http
│
├── achei.db
├── requirements.txt
├── README.md

## Descrição dos Diretórios

### app/

Contém o backend da aplicação, desenvolvido com FastAPI.

Esse diretório é responsável pelas rotas, regras de negócio, validações, permissões de usuário e comunicação com o banco de dados.

Arquivos principais:

main.py: arquivo principal da API. Contém as rotas do sistema, como login, cadastro de postos, registro de itens, retirada de itens e consulta de históricos.
db.py: responsável pela conexão com o banco SQLite, criação das tabelas e inserção dos usuários de demonstração.
schemas.py: define os modelos de entrada de dados usados pelo FastAPI para validar as requisições.
__init__.py: indica que a pasta app deve ser tratada como um pacote Python.

###frontend/

Contém a interface do sistema, desenvolvida com HTML, CSS e JavaScript.

Esse diretório é responsável pela interação do usuário com o sistema, exibindo telas, formulários, listas e botões de ação.

Arquivos principais:

index.html: estrutura principal da interface.
style.css: estilização visual do sistema, incluindo o tema em azul suave e a responsividade.
script.js: controla o login, permissões por perfil, exibição das funcionalidades e chamadas para a API do backend.
README_FRONTEND.md: instruções específicas sobre o funcionamento do frontend.

### tests/

Contém os testes automatizados do backend.

Arquivos principais:

test_crud.py: testa os principais fluxos do sistema, incluindo o CRUD de posto, item e termo de retirada.

###scripts/

Contém arquivos auxiliares para demonstração e teste da API.

Arquivos principais:

exemplo_requisicoes.http: arquivo com exemplos de requisições HTTP para testar as rotas sem precisar usar o frontend ou a documentação automática /docs.

###achei.db

Arquivo do banco de dados SQLite.

Ele é criado automaticamente quando o backend é executado.

requirements.txt

Lista as dependências Python necessárias para rodar o backend.

Exemplo de uso:
pip install -r requirements.txt

README.md

Arquivo principal de documentação do projeto.

Contem instruções de instalação, execução, descrição das funcionalidades, tecnologias utilizadas e organização do sistema.

## Arquitetura de Dados

O sistema utiliza SQLite como banco de dados local e o módulo sqlite3 do Python para executar as operações no banco.

As consultas são feitas com SQL parametrizado, usando ? nos comandos SQL. Essa abordagem evita a concatenação direta de dados nas consultas e reduz riscos de consultas inseguras.

O banco é criado automaticamente pelo arquivo: app/db.py
E armazenado no arquivo: achei.db

# 6. Equipe

* Christian Miguel Lopes
* José Geraldo Caria da Silva
* Pedro Henrique Gonçalves Reis
