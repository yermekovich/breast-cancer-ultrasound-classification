# Breast Ultrasound Image Classification

Классификация ультразвуковых изображений молочной железы на три класса: **normal**, **benign**, **malignant**. Transfer learning на ResNet18 и ResNet50, веб-приложение на Streamlit для классификации загруженного снимка.

> Учебный проект (Astana IT University). Не является медицинским изделием и не предназначен для диагностики.

## Результаты

Лучшая модель на тестовой выборке:

| Метрика | Значение |
| --- | --- |
| Accuracy | 89.87% |
| F1-score | 89.83% |
| Precision | 90.07% |
| Recall | 89.87% |

## Что внутри

- `aml.ipynb` — подготовка данных, аугментация, обучение и сравнение ResNet18 и ResNet50
- `app.py` — Streamlit-приложение
- `report.pdf` — отчёт по проекту
- `requirements.txt` — зависимости

## Данные

Kaggle: *Breast Ultrasound Images Dataset*. Данные в репозиторий не включены, скачайте их отдельно и положите в `data/`.

## Запуск

```bash
git clone https://github.com/yermekovich/breast-cancer-ultrasound-classification
cd breast-cancer-ultrasound-classification
pip install -r requirements.txt
streamlit run app.py
```

## Подход

1. Предобработка и аугментация изображений
2. Дообучение предобученных ResNet18 и ResNet50
3. Оценка: precision, recall, F1-score, accuracy
4. Деплой лучшей модели в Streamlit

## Ограничения

Небольшой публичный датасет, один источник данных, нет внешней валидации. Результаты нельзя переносить на клинические данные без дополнительной проверки.
