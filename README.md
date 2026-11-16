# Tasks Flask CRUD

API REST simples de gerenciamento de tarefas (CRUD) desenvolvida com **Flask**, com testes automatizados usando **pytest** e especificação OpenAPI/Swagger (`swagger.yaml`).

## Funcionalidades

- `POST /tasks` — Criar uma nova tarefa
- `GET /tasks` — Listar todas as tarefas
- `GET /tasks/<id>` — Obter detalhes de uma tarefa específica
- `PUT /tasks/<id>` — Atualizar uma tarefa existente
- `DELETE /tasks/<id>` — Remover uma tarefa

## Tecnologias utilizadas

- Python 3
- [Flask](https://flask.palletsprojects.com/)
- [pytest](https://docs.pytest.org/) & `requests` (testes automatizados em `tests.py`)

## Como executar

1. Crie e ative um ambiente virtual:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/macOS
   # venv\Scripts\activate   # Windows
   ```

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

3. Execute a aplicação:
   ```bash
   python app.py
   ```

4. Para rodar os testes (com o servidor em execução):
   ```bash
   pytest tests.py
   ```