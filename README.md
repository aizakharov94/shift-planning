# Предсказание спроса и планирование рабочих смен
Продукт представляет собой реализацию проекта «Предсказание спроса и планирование рабочих смен» в рамках зимней школы [CompTech School 2022](https://comptechschool.com/).

// перечислить все папки репозитория (первого уровня) и что в них лежит


-  '''data''' -
- docs - 
- Stage 1. -
- Stage 2. -
- Stage 3. -
- 
## Назначение
Основная цель продукта - спланировать привлечение такого количества курьеров на неделю вперед по дням и по часам каждого дня недели, чтобы полностью компенсировать дневные колебания спроса, учитывая утренние и вечерние пики.

## Принцип работы

// в двух-трех абзацах описать работу Продукта, добавить схемы при необходимости. Использовать информацию из Vision

[Схема проекта](./docs/source/common_view_of_project.svg)

## Целевая аудитория (пользователи продукта)

- Владелец продукта: Сбермаркет.
- Пользователи: продуктовые менеджеры, которые на основе выдаваемого результата продукта, принимают решения о найме курьеров.


## Установка и настройка

Описание операций:
#### main
Для установки необходимых библиотек необходимо выполнить:
```shell
  pip install -r requirements.txt
```

Для получения прогноза спроса, числа курьеров и распределения по сменам на следующую неделю необходимо подключить файл ```main.py```. После этого запустить функцию:
```python
  main() -> (pd.DataFrame, pd.DataFrame)
```

#### Stage 1.
Для получения распределения заказов на следующую неделю неделю необходимо подключить файл ```stage1_main.py```. 
После этого запустить функцию:
```python
  get_next_week(path: str) -> pd.DataFrame
```
#### Stage 2.
Для получения оптимального распределения курьеров на следующую неделю неделю необходимо подключить файл ```stage2_main.py```. 
После этого запустить функцию:
```python
  get_optimal_partners(path_orders: str, path_partners_delays: str, pred_orders: pd.DataFrame) -> pd.DataFrame
```
#### Stage 3.
Для получения оптимального распределения курьеров по сменам необходимо подключить файл ```stage3_main.py```. 
После этого запустить функцию:
```python
  get_partners_distribution(pred_partners: pd.DataFrame) -> pd.DataFrame
```


#### Зависимости

При создании системы команда использовала язык программирования python и его библиотеки:
- numpy
- pandas
- matplotlib
- scikit-learn
- category-encoders
- holidays
- ortools

## Команда
- Захаров Андрей - Куратор
- Ратушный Алексей - Data Scientist
- Майоров Константин - Data Scientist
- Кузнецов Никита - Data Scientist
- Желтова Кристина - Data Scientist
- Завьялов Фёдор - Data Scientist
- Мельникова Маргарита - Data Scientist
- Сарыглар Орлан - технический писатель
