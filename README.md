# VK-Techno-Test
# Классификация временных рядов с использованием LSTM и балансировка классов

Этот проект предназначен для классификации временных рядов с помощью рекуррентной нейронной сети LSTM, с предварительной балансировкой классов с использованием алгоритма ADASYN. Проект позволяет предсказывать вероятность классов на тестовых данных и готовит файл для отправки с результатами.

## Структура проекта

- **Обработка данных**:
  - Данные для обучения находятся в файле `train.parquet`.
  - Тестовые данные находятся в файле `test.parquet`.
  - Выполняется подготовка данных, включая их масштабирование, приведение к необходимой форме для модели и балансировку классов с использованием ADASYN.
  
- **Модель**:
  - Используется двунаправленная LSTM модель с слоями Dropout для регуляризации.
  - Модель обучается с использованием кросс-энтропии для многоклассовой классификации и оптимизируется с помощью Adam.

- **Балансировка классов**:
  - Алгоритм ADASYN из библиотеки `imbalanced-learn` применяется для генерации дополнительных данных для меньшего класса с целью устранения дисбаланса классов.

- **Анализ данных**:
  - Визуализация распределения классов до и после балансировки осуществляется с помощью библиотек `Matplotlib` и `Seaborn`.

- **Предсказания**:
  - Тестовые данные подготавливаются и проходят через обученную модель для получения вероятностей классов.
  - Результаты сохраняются в файл `submission.csv` с предсказанными вероятностями для каждого объекта тестовой выборки.

## Требуемые библиотеки

Для запуска проекта необходимо установить следующие библиотеки:

- `tensorflow` и `keras` для создания и обучения LSTM модели.
- `imbalanced-learn` для балансировки данных с помощью ADASYN.
- `pandas` для работы с данными в формате Parquet.
- `numpy` для работы с массивами данных.
- `matplotlib` и `seaborn` для визуализации.
  
![загруженное (6)](https://github.com/user-attachments/assets/21096993-7b6c-4ddd-98fc-38ab80102334)

  
![загруженное (7)](https://github.com/user-attachments/assets/a11baba9-00e4-44ba-b5a7-6da41bd847e7)

