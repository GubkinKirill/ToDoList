# ToDoList

ToDoList - это простое приложение для управления задачами, созданное с использованием FastAPI и SQLAlchemy.

## Установка

1. Клонируйте репозиторий:
    ```bash
    git clone https://github.com/GubkinKirill/ToDoList.git
    cd ToDoList
    ```

2. Создайте и активируйте виртуальное окружение:
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. Установите зависимости:
    ```bash
    pip install -r requirements.txt
    ```

4. Запустите приложение:
    ```bash
    uvicorn app.main:app --reload
    ```

## Использование

### Создание задачи

Отправьте POST-запрос на `/tasks/` с телом запроса в формате JSON:
```json
{
  "title": "Прочитать книгу",
  "description": "Закончить чтение книги по FastAPI",
  "completed": false
}
```

### Получение списка задач

Отправьте GET запрос на /tasks/. Ответ будет содержать список задач:
```json
[
  {
    "id": 1,
    "title": "Прочитать книгу",
    "description": "Закончить чтение книги по FastAPI",
    "completed": false
  }
]
```

### Получение задачи по ID

Отправьте GET запрос на /tasks/1. Ответ будет содержать задачу с ID 1:
```json
{
  "title": "Прочитать книгу",
  "description": "Закончить чтение книги по FastAPI",
  "completed": false
}
```

### Удаление задачи

Отправьте DELETE запрос на /tasks/1. Ответ будет содержать удаленную задачу:
```json
{
  "title": "Прочитать книгу",
  "description": "Закончить чтение книги по FastAPI",
  "completed": false
}
```