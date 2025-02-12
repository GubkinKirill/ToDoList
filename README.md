# ToDoList

ToDoList - это простое приложение для управления задачами, созданное с использованием FastAPI и SQLAlchemy.

## Установка

1. Клонируйте репозиторий:
    ```bash
    git clone https://github.com/yourusername/ToDoList.git
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