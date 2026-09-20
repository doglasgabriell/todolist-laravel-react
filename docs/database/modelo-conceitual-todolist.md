# Modelo conceitual - Todolist
    Representação das entidades, atributos e regras de negócio através do modelo conceitual

## Elementos usados
- Entidades - Retângulos (Task & User)
  - Representação das tabelas principais para o relacionamento entre ambas
- Chaves identificadora (Circulo escuro)
    - id -> Identificador único de cada registro da tabela. Seu valor não deve se repetir dentro daquela tabela, permitindo diferenciar cada registro
- Relacionamento **User cria task**
    - Um usuário pode criar nenhuma ou várias tarefas, cada tarefa pertence restritamente ao usuário que gerou-a
        - User(1:N) --- CRIA --- (1:1) Task

## Entidades criadas
**Criada duas entidades para representar as regras de negócios do sistema:**

### user
    Representa o usuário que possui o acesso ao sistema podendo gerenciar as suas próprias tarefas, desde criar, atualizar, ler e deletar 

#### Atributos
| Campo | Descrição |
| ----- | --------- |
| id    | Identificador único do usuário |
| name | Nome do usuário|
| email | Email de acesso do usuário |
| password | Senha de acesso do usuário ao sistema |



### task
    Representa a tarefa criada pelo usuário podendo ser gerenciada pelo mesmo

#### Atributos
| Campo | Descrição |
| ----- | --------- |
| id    | Identificador único da tarefa |
| title | Titulo da tarefa |
| description | Descrição da tarefa|
| created_date | Data de criação da tarefa |
| priority | Prioridade da tarefa, recebendo valores como: Urgente, Alta, média e Baixa
| status | Status da tarefa recebendo valores como: Realizada, Não realiaza e em andamento


