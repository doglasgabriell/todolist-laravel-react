# todolist-laravel-react
## Aplicação ToDo List fullstack com: API REST em Laravel (PHP) no backend e interface interativa em React (Vite) no frontend com CRUD.

### 🚀 **Técnologias utilizadas**
- **Backend:** PHP, Laravel, MySQL
- **Frontend:** React, vite, Tailwindcss, CSS
- **Arquitetura:** API REST, Padrão MVC

### 🛠 **Funcionalidades CRUD**
- **CREATE:** Adicionar novas tarefas (POST /api/...)
- **READ:** Busca e exibição das tarefas cadastradas no banco (GET /api/...)
- **UPDATE:** Alternar status da tarefa/nome/descrição e prioridade (PUT /api/.../{id})
- **DELETE:** Remoção de registros da lista, todos ou especificos (DELETE /api/.../{id})

#### ❓ **Pré requisitos:** 
    PHP >= 8.2 & Composer instalado
    Node.js >= 18 e npm instalados


### ⚙ **Configurar o Backend (Laravel)**
```bash
    cd backend
    composer install
    cp .env.example .env
    php artisan key:generate
    php migrate
    php artisan serve  
```
* O laravel iniciará em [http://127.0.0.1:8000](http://127.0.0.1:8000)

### ⚙ **Configurar o Frontend (React/Vite)**
```bash
    cd frontend
    npm i ou npm install
    npm run dev
```
O React iniciará em [http://localhost:5173](http://localhost:5173)

### 📍 **Endpoints da API**

| Método | Rota | Descrição | 
| ------ | ---- | --------- |
| GET    | /api/.../{id} | Retorna as tarefas ou uma tarefa especifica
| POST | /api/... | Cria uma nova tarefa
| PUT | /api/.../{id} | Atualiza informações da tarefa
| DELETE | /api/.../{id} | Deleta uma ou todas as tarefas


