# Авиаперевозки: Аналитический дашборд в Apache Superset

## Описание проекта
Проект представляет собой BI-дашборд для анализа данных авиаперевозок на основе демонстрационной базы данных Postgres Pro. Дашборд позволяет отслеживать ключевые показатели бизнеса: общую выручку, загруженность рейсов, статусы рейсов и поведение пассажиров.

![Dashboard Screenshot]<img width="1905" height="877" alt="image" src="https://github.com/user-attachments/assets/c2a9db4c-4160-4700-b001-76666cc49d31" />
)

## Структура репозитория
- `charts/` — YAML-файлы с конфигурациями визуализаций
- `dashboards/` — YAML-файл с конфигурацией дашборда
- `datasets/` — YAML-файлы с настройками датасетов
- `schema.sql` — дамп структуры демонстрационной базы данных
- `superset_config.py` — пример конфигурации Superset

## Стек
- **BI**: Apache Superset 4.x (установка на Windows)
- **СУБД**: PostgreSQL
- **Данные**: Демо-база «Авиаперевозки» (Postgres Pro)

## Как развернуть проект
1. Установите Apache Superset согласно [официальной инструкции](https://superset.apache.org/docs/installation/installing-superset-from-scratch).
2. Восстановите структуру базы данных из файла `schema.sql`.
3. Загрузите демонстрационные данные в PostgreSQL (опционально, т.к. дашборд можно импортировать и без данных).
4. Импортируйте дашборд в Superset: `Settings` -> `Import Dashboards`.

## Ключевые метрики дашборда
- **Total Revenue**: Общая выручка.
- **Total Bookings / Passengers**: Количество бронирований и пассажиров.
- **Avg Check / Delay**: Средний чек и средняя задержка рейсов.
- **Flight Status Distribution**: Распределение рейсов по статусам.
