# Практика с трансформерными моделями для NLP

## Цель

Научиться работать с трансформерными моделями и применять их для различных задач обработки естественного языка (NLP).

---

## Описание / Пошаговая инструкция выполнения домашнего задания

### 1. Выбор датасета

В качестве данных используйте датасет **RuCoLA** для русского языка:  
[https://github.com/RussianNLP/RuCoLA](https://github.com/RussianNLP/RuCoLA)

- В качестве обучающей выборки возьмите файл `in_domain_train.csv`.
- В качестве тестовой выборки — `in_domain_dev.csv`.

Дополнительно разбейте `in_domain_train` на **train** и **val** (валидационную выборку).

---

### 2. Fine‑tuning BERT‑подобных моделей

Зафайнтюньте и протестируйте одну из моделей семейства **RuBERT** или **RoBERTa** на данной задаче.  
Вы можете взять любую предобученную модель с сайта [Hugging Face](https://huggingface.co/). Рекомендуемые варианты:

- [sberbank-ai/ruBert-base](https://huggingface.co/sberbank-ai/ruBert-base)
- [sberbank-ai/ruBert-large](https://huggingface.co/sberbank-ai/ruBert-large)
- [DeepPavlov/rubert-base-cased](https://huggingface.co/DeepPavlov/rubert-base-cased)
- [sberbank-ai/ruRoberta-large](https://huggingface.co/sberbank-ai/ruRoberta-large)
- [xlm-roberta-base](https://huggingface.co/xlm-roberta-base)

---

### 3. Few‑shot / Zero‑shot подход с GPT‑3

Возьмите модель **RuGPT‑3** (base или large) и решите задачу с помощью **few‑shot** или **zero‑shot** методов.

Необходимо выполнить:

- **а)** Перебрать несколько вариантов **затравок** (промптов / шаблонов).
- **б)** Протестировать различное количество **few‑shot примеров**: `0, 1, 2, 4`.

---

### 4. Fine‑tuning T5

Обучите и протестируйте модель **RuT5** на данной задаче.  
Пример fine‑tune можно найти в официальном репозитории:  
[https://github.com/RussianNLP/RuCoLA/blob/main/baselines/finetune_t5.py](https://github.com/RussianNLP/RuCoLA/blob/main/baselines/finetune_t5.py)

---

### 5. Сравнение результатов

Сравните полученные результаты всех подходов между собой.

---

## Критерии оценки

| Что оценивается | Баллы |
|----------------|-------|
| Fine‑tuning BERT‑подобной модели | 3 |
| Реализация few‑shot / zero‑shot с GPT‑3 | 4 |
| Fine‑tuning RuT‑5 | 3 |