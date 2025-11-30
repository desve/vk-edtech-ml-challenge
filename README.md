# VK EdTech ML Challenge: прогноз эффективности рекламных кампаний

Репозиторий с end‑to‑end решением задачи VK EdTech ML Challenge: по истории показов рекламы и профилям пользователей предсказать эффективность будущих рекламных кампаний.  
Цель — оценить вероятность того, что хотя бы один / два / три пользователя из аудитории совершат целевое действие.

Локальная метрика качества (официальный `metrics.py`, Smoothed Mean Log Accuracy Ratio, меньше — лучше): **37.51%** на валидации.

---

## Данные

Используются четыре табличных файла в формате TSV (разделитель — табуляция):

- `users.tsv` — пользователи:
  - `user_id`, `sex`, `age`, `city_id`.
- `history.tsv` — история показов:
  - `hour`, `cpm`, `publisher`, `user_id`.
- `validate.tsv` — описание кампаний для валидации:
  - `cpm`, `hour_start`, `hour_end`, `publishers`, `audience_size`, `user_ids`.
- `validate_answers.tsv` — ответы для валидации:
  - `at_least_one`, `at_least_two`, `at_least_three`.

Файлы данных **не хранятся в репозитории**. Их нужно скачать с официальной страницы задачи VK EdTech ML Challenge и положить локально, например так:
```
data/raw/
users.tsv
history.tsv
validate.tsv
validate_answers.tsv
```


