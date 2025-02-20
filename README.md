# API de Gerenciamento de Tarefas

Esta é uma API RESTful simples para gerenciamento de tarefas (To-Do List) construída com Flask. Permite criar, listar, atualizar e deletar tarefas.

## Tecnologias Utilizadas

- Python 3.x
- Flask 2.3.0
- Flask-SQLAlchemy 3.1.1
- Flask-Cors 3.0.10
- Werkzeug 2.3.0

## Estrutura do Projeto

```
project/
├── models/
│   └── task.py         # Classe Task
├── app.py             # Arquivo principal da aplicação
├── requirements.txt   # Dependências do projeto
└── openapi.yaml       # Documentação OpenAPI
```

## Instalação

1. Clone o repositório:
```bash
git clone <url-do-repositorio>
cd <nome-do-diretorio>
```

2. Crie um ambiente virtual:
```bash
python -m venv venv
```

3. Ative o ambiente virtual:
- Windows: `venv\Scripts\activate`
- Linux/Mac: `source venv/bin/activate`

4. Instale as dependências:
```bash
pip install -r requirements.txt
```

5. Execute a aplicação:
```bash
python app.py
```

A API estará disponível em `http://127.0.0.1:5000`.

## Endpoints da API

### Listar todas as tarefas
```
GET /tasks
```
Retorna uma lista de todas as tarefas e o total.

### Criar nova tarefa
```
POST /tasks
```
Body:
```json
{
    "title": "Título da tarefa",
    "description": "Descrição opcional"
}
```

### Obter uma tarefa específica
```
GET /tasks/{id}
```

### Atualizar uma tarefa
```
PUT /tasks/{id}
```
Body:
```json
{
    "title": "Novo título",
    "description": "Nova descrição",
    "completed": true
}
```

### Deletar uma tarefa
```
DELETE /tasks/{id}
```

## Modelo de Dados

A classe `Task` (em `models/task.py`) possui os seguintes atributos:
- `id`: Inteiro (único)
- `title`: String (obrigatório)
- `description`: String (opcional)
- `completed`: Booleano (padrão: false)

## Documentação OpenAPI

A especificação completa da API está disponível no arquivo `swagger.yaml`.

## Uso

Exemplo com curl para criar uma tarefa:
```bash
curl -X POST http://127.0.0.1:5000/tasks \
-H "Content-Type: application/json" \
-d '{"title": "Minha primeira tarefa", "description": "Fazer algo importante"}'
```

Exemplo para listar tarefas:
```bash
curl http://127.0.0.1:5000/tasks
```

## Desenvolvimento

Para rodar em modo debug:
```bash
python app.py
```

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

## Contato

Para dúvidas ou sugestões, entre em contato através do [gugasilva.machado@gmail.com](mailto:gugasilva.machado@gmail.com).