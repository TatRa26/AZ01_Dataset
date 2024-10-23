# AZ01_Dataset

# Data Analysis with Pandas

Этот проект демонстрирует использование библиотеки Pandas для анализа данных из CSV файлов. Представлены два скрипта, которые выполняют различные задачи анализа данных.

## Скрипт 1: Обзор данных из файла 'The Rise Of Artificial Intelligence2.csv'

### Описание

Первый скрипт предназначен для первоначального анализа данных из файла `The Rise Of Artificial Intelligence2.csv`. Он выполняет следующие функции:

1. **Импорт библиотеки Pandas**: Pandas - это мощный инструмент для обработки и анализа данных.
2. **Загрузка данных**: Чтение данных из CSV файла в объект DataFrame.
3. **Просмотр первых строк**: Вывод первых нескольких строк для быстрого ознакомления с содержимым и структурой данных.
4. **Сводная информация**: Выводит краткую сводку о DataFrame, включая количество непустых записей, типы данных столбцов и использование памяти.
5. **Статистический анализ**: Генерирует описательную статистику для числовых столбцов, включая среднее, стандартное отклонение, минимальные и максимальные значения.


import pandas as pd

# Чтение CSV файла в DataFrame
df = pd.read_csv('The Rise Of Artificial Intelligence2.csv')

# Отображение первых строк DataFrame
print(df.head())

# Вывод краткой информации о DataFrame
print(df.info())

# Генерация описательной статистики для числовых столбцов
print(df.describe())


## Скрипт 2: Анализ средней зарплаты по городам

### Описание

Второй скрипт выполняет анализ данных из файла `dz.csv`, вычисляя среднюю зарплату по городам. Он включает в себя следующие шаги:

1. **Импорт библиотеки Pandas**: Используется для загрузки и обработки данных.
2. **Загрузка данных**: Загружает данные из CSV файла в DataFrame.
3. **Группировка и вычисление** : Группирует данные по столбцу `City` и вычисляет среднее значение зарплаты для каждого города.
4. **Вывод результата**: Отображает среднюю зарплату для каждого города.

### Код


import pandas as pd

# Загрузка данных из CSV файла
df = pd.read_csv('dz.csv')

# Группировка данных по городу и вычисление средней зарплаты
average_salary_by_city = df.groupby('City')['Salary'].mean()

# Вывод результата
print(average_salary_by_city)


## Требования

- Python 3.x
- Библиотека Pandas

Убедитесь, что все необходимые зависимости установлены, прежде чем запускать скрипты. Эти скрипты предоставляют базовую функциональность для анализа данных и могут служить отправной точкой для более сложных исследований.


Этот README файл предоставляет четкое объяснение каждого скрипта, включая их функциональность и цели. Такой подход помогает другим разработчикам понять, как и зачем использовать ваш код.