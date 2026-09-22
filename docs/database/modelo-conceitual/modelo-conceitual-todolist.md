# Modelo conceitual - Todolist
    Representação das entidades, atributos e regras de negócio através do modelo conceitual

## Elementos usados
- Entidades (Retângulos)
  - Representação das tabelas principais para o relacionamento entre ambas
- Chaves identificadora (Circulo escuro)
    - id -> Identificador único de cada registro da tabela. Seu valor não deve se repetir dentro daquela tabela, permitindo diferenciar cada registro
- Relacionamento
    - Um usuário pode criar nenhuma ou várias tarefas, cada tarefa pertence restritamente ao usuário que gerou-a e uma tarefa pode ter uma prioridade/status e cada prioridade/status podem ter varias tarefas relacionadas.
        - users(1:N) --- CRIA --- (1:1) task
        - Priorities(1:N) --- TEM --- (1:1) task
        - Status(1:N) --- TEM --- (1:1) task 

## Entidades criadas
**Foram criadas 4 entidades para representar as regras de negócios do sistema:**

### users
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
| priorities_id | Idenficador único da tabela priorities relacionando uma tarefa com o prioridade | 
| status_id | Identificador único do status relacionando uma tarefa com o status de progressão |

### priorities
    Representa as prioridades relacionadas a cada tarefa 

#### Atributos
| Campo | Descrição |
| ----- | --------- |
| id    | Identificador único da prioridade |
| name  | nome da prioridade (Alta, média, Baixa) |

### status
    Reprensenta o status de conclusão da tarefa

#### Atributos
| Campo | Descrição |
| ----- | --------  |
| id    | Identificador único da prioridade |
| name  | nome do status (Pendente, Realizado)
