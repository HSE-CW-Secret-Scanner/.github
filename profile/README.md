# HSE-CW-Secret-Scanner
Курсовая работа на тему  
*"Автоматический анализ репозиториев на наличие конфиденциальной информации с помощью методов машинного обучения"*
### Описание
Работа представляет собой MVP гибридной модели для анализа исходного кода корпоративных репозиториев на наличие секретов (API-ключей, паролей, токенов доступа) с использованием машинного обучения.  
Она обеспечивает:  
- мониторинг новых коммитов в реальном времени,
- сканирование на наличие различных типов секретов,
- интеграцию с GitHub через Webhooks для отслеживания изменений в репозиториях.
  
Результаты сканирования сохраняются в PostgreSQL, а визуализация данных осуществляется через дашборды Grafana.
### Технологический стек
##### Сканирование
Python 3.10 (requests, SQLAlchemy, pandas)  
noseyparker  
LLaMa3.1 (Ollama)  
##### Оркестрация
Airflow 2.5.3  
##### Хранение данных
PostgreSQL 13 
##### Мониторинг и визуализация данных
Prometheus  
Grafana  
##### Оповещения и отчеты
Telegram
### Репозитории
|Ссылка|Описание|
|-|--------|
|https://github.com/HSE-CW-Secret-Scanner/airflow-dags| DAG'и для сканирования репозиториев и отправки уведомлений в Telegram|
|https://github.com/HSE-CW-Secret-Scanner/llm-testing| Тестирование больших языковых моделей (LLM) с помощью Ollama|
|https://github.com/HSE-CW-Secret-Scanner/kafka-event-manager| Потоковая обработка событий с помощью Kafka|
|https://github.com/HSE-CW-Secret-Scanner/secrets-db|Dump базы данных для хранения секретов|
|https://github.com/HSE-CW-Secret-Scanner/kafka-deployment| Развертывание сервера Kafka|
|https://github.com/HSE-CW-Secret-Scanner/airflow-deployment| Развертывание сервера Airflow, Prometheus, Grafana|
