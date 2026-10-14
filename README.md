# PestCLEF: извлечение графов знаний из текста

Учебный проект по извлечению связей из текстов о вредителях растений. Метод: CRF и словарь → концепты → LightGBM → граф → CSV. Код, объяснения и анализ результатов находятся в [ноутбуке](pestclef_pipeline_kg.ipynb).

## Запуск

1. Установите зависимости для Python 3.11: `pip install -r requirements.txt`. На macOS для LightGBM также нужен `libomp`.
2. Скачайте [данные соревнования](https://www.kaggle.com/competitions/pest-clef-2026/data): JSON train/dev/test положите в корень проекта, тексты - в `EPOP_documents/train`, `dev`, `test`. Тексты доступны отдельно по ссылке **Download** на странице данных.
3. Проверьте пути в ноутбуке, выберите ядро с установленными зависимостями и нажмите **«Выполнить всё»**. Первый запуск обучает модели, повторный использует кэш.

## Результат

Результаты сохраняются в `outputs/fixed/`. Файл для Kaggle — [submission_candidate.csv](outputs/fixed/submission_candidate.csv): public **0.57890**, private **0.58085**.

Презентация: [PPTX](PestCLEF_SPbU.pptx), [PDF](PestCLEF_SPbU.pdf).
