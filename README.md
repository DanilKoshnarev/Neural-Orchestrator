
# 🧠 Neural Orchestrator  
> Менеджер для интеграции с различными нейросетями (ChatGPT, Gemini, HoppyCopy и другие).
```
           ,--,                                                       
    ,--.'|                                                       
 ,--,  | :                                                       
 |  |  : '                                                       
 :  :  | |  ,--.--.        ,---.                                 
 :  |  ' ; /       \      /     \                                
 |  :  | |.--.  .-. |    /    /  |                               
 |  |  |/  \__\/: . .   .    ' / |                               
 '  :  ;   ," .--.; |   '   ;   /|                               
 |  ,/   /  /  ,.  |   '   |  / |                               
 '--'   ;  :   .'   \  |   :    |                               
         |  ,     .-./   \   \  /                                
          `--`---'        `----'                                 
       ,---.              .---.         ,---.                    
      /     \            /.  ./|       '   ,'\                   
     /    /  |        .-' . ' |      /   /   |                  
    .    ' / |       /___/ \: |     .   ; ,. :                  
    '   ;   /|    .-'.. '   ' .     '   | |: :                  
    '   |  / |   /___/ \:     '     '   | .; :                  
    |   :    |    .   \  ' .\        |   :    |                 
     \   \  /      \   \   ' \        \   \  /                  
      `----'        \   \  |  |        `----'                   
                      \   \ |                                  
                       '---"

```
## **Описание**
**Neural Orchestrator** — это универсальный менеджер для работы с нейросетями. Приложение поддерживает более 10 нейросетей, включая ChatGPT, Gemini, HoppyCopy, и обеспечивает простую интеграцию с ними.  

Проект реализован на Python с использованием многопоточности для оптимальной работы и минимизации задержек.  

---

## **Функционал**
- Обработка запросов через многопоточность (до 5 потоков одновременно).  
- Подключение к более чем 10 нейросетям (ChatGPT, Gemini, Bing, Claude, и другие).  
- Кеширование запросов и ответов через Redis.  
- API на базе FastAPI для удобного взаимодействия с приложением.  
- Легко расширяемая архитектура.

---

## **Требования**
- Python 3.10+  
- Redis  

---

## **Установка и запуск**

### 1. **Клонируйте репозиторий**
```bash
git clone https://github.com/your-repo/Neural-Orchestrator.git
cd Neural-Orchestrator

2. Создайте виртуальное окружение

python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

3. Установите зависимости

pip install -r requirements.txt

4. Запустите Redis

docker run -d -p 6379:6379 redis

5. Запустите FastAPI-сервер

uvicorn src.app.main:app --reload

```

## Использование

Пример запроса:

Отправьте POST-запрос на /query через Postman, Curl или любой другой инструмент:

curl -X POST http://127.0.0.1:8000/query \
-H "Content-Type: application/json" \
-d '{"prompt": "Hello, world!", "service": "chatgpt"}'

Пример ответа:

{
  "service": "chatgpt",
  "prompt": "Hello, world!",
  "response": "Hi there!"
}




## Структура проекта
```bash
src/
├── app/
│   ├── main.py              # Точка входа FastAPI
│   ├── config.py            # Конфигурации приложения
├── domain/
│   ├── models/
│   │   ├── query.py         # Модель запросов
│   │   ├── service_enum.py  # Перечисление поддерживаемых нейросетей
├── application/
│   ├── use_cases/
│   │   ├── process_query.py # Логика обработки запросов
├── infrastructure/
│   ├── redis_cache.py       # Работа с Redis
│   ├── service_clients/     # Клиенты для взаимодействия с API нейросетей
│   │   ├── chatgpt_client.py
│   │   ├── gemini_client.py
│   │   ├── ...
├── interfaces/
│   ├── api/
│   │   ├── router.py        # Роутеры для FastAPI
├── tests/
│   ├── unit/                # Юнит-тесты
│   ├── integration/         # Интеграционные тесты
│   ├── e2e/                 # End-to-End тесты

```

## Поддерживаемые нейросети

1. ChatGPT


2. Gemini


3. HoppyCopy


4. Bing AI


5. Claude


6. Perplexity


7. YouChat


8. DeepL


9. Jasper


10. CopyAI

## Контакты

Для вопросов и предложений:
📧 4youdanchiknew@gmail.com



