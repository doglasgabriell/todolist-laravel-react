
# Modelo logico - Todolist
    Representação lógica das entidades e relacionamentos definindo os atributos, tipos de dados e chaves

## Elementos usados
- Entidades (Task & User)
  - Representação das tabelas principais para o relacionamento entre ambas
- Chaves identificadora
    - id -> Identificador único de cada registro da tabela. Seu valor não deve se repetir dentro daquela tabela, permitindo diferenciar cada registro.
- Atributos (title, name, description [...])
    - Campos que armazenarão as informaçõs respectivas de cada tabela. **Exemplo:** 
        - Atributo **name** recebe os nome de cada usuário logado: Lavínia, Dôglas, Gleice, Dalmo...
- Chaves estrangeiras (FK Foreign key)
    - Relaciona um(s) registro(s) de uma tabela a outra. **Exemplo:** Usuário se relaciona com Task, pois, um usuário pode criar varias tarefas e cada tarefa está relacionada a cada usuário.

## Tabelas criadas
    Tabela user & task criadas para a representação das regras de negócios


### user
    Representa o usuário que possui o acesso ao sistema podendo gerenciar as suas próprias tarefas, desde criar, atualizar, ler e deletar 


#### Atributos
| Campo | Tipo | Chave | Descrição |
| ----- | ------ | ---- | --------- |
| id    | Integer | PK |Identificador único do usuário, representado pelo tipo Integer |
| name | Varchar | - | Nome do usuário recebendo o tipo texto|
| email | Varchar | - | Email de acesso do usuário do tipo texto |
| password | Varchar | - | Senha de acesso do usuário ao sistema |


### task
    Representa a tarefa criada pelo usuário podendo ser gerenciada pelo mesmo

#### Atributos
| Campo | Tipo | Chave | Descrição |
| ----- | ---- |  ---- |--------- |
| id    | Integer| PK | Campo identificador da tabela task aceitando apenas entradas do tipo inteiro (número) |
| title | Varchar | - | Titulo referenciado a tarefa do tipo string(texto)|
| description | Varchar | - | Descrição da tarefa, tipo texto |
| created_date | Date | - | Data de criação da tarefa |
| priority | Varchar | - | Prioridade da tarefa, Valores permitidos: Urgente, Alta, média e Baixa
| status | Varchar | - | Status da tarefa Valores permitidos: Realizada, Não realizado e em andamento |
| user_id | Integer | FK | Chave estrangeira que identifica o usuário responsável pela tarefa e referencia o id da tabela user.
