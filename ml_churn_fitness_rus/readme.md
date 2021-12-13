## Учебный проект "Анализ признаков клиентов фитнес-сети, попавших в отток, и построение моделей прогнозирования оттока"
[Открыть проект в nbviewer](https://nbviewer.org/github/Emiranunuka/Yandex_Practicum_Data_Analyst_Training_Projects_Rus/blob/main/ml_churn_fitness_rus/avdonina_ml_churn_fitness_rus.ipynb)
### Описание проекта и задачи
Сеть фитнес-центров разрабатывает стратегию взаимодействия с клиентами на основе аналитических данных. Хотят получить улучшения по проблеме оттока клиентов. 
Считают, что клиент попал в отток, если за последний месяц ни разу не посетил спортзал.

Цель работы: провести анализ клиентских анкет с признаками и подготовить план действий по удержанию клиентов.

Задачи:
* спрогнозировать вероятность оттока (на уровне следующего месяца) для каждого клиента;
* сформировать типичные портреты клиентов: выделить несколько наиболее ярких групп и охарактеризовать их основные свойства;
* проанализировать основные признаки, наиболее сильно влияющие на отток;
* сформулировать основные выводы и разработать рекомендации по повышению качества работы с клиентами:
  - выделить целевые группы клиентов;
  - предложить меры по снижению оттока;
  - определить другие особенности взаимодействия с клиентами.
### Заказчик
Отдел по работе с клиентами.
### Стек
Python, pandas, scipy, matplotlib, plotly express, seaborn, sklearn.
### Анализ
Анализ корреляции между признаками, указанными в клиентской анкете: возраст, пол, "стаж" в фитнес-сети, длительность текущего абонемента, остаток текущего абонемента, средняя частота
посещения фитнеса в неделю вообще и за последний месяц, суммарная выручка от доп.услег фитнес-центра, рекомендация друга, посещение групповых занятий, работа в компании-партнере,
близкое проживание, и фактом оттока. 

Обучение с учителем. Стандартизация датафрейма. Разделение на обучающую и валидационную выборки. Обучение моделей прогнозирования целевого признака на основе алгоритмов 
логистической регрессии (LogisticRegression) и случайного леса (RandomForestClassifier). Прогнозирование класса (значений целевой переменной churn) на основе признаков валидационной 
выборки. Оценка ошибок моделей.

Обучение без учителя. Определение числа кластеров с помощью метода агломеративной иерархической кластеризации (дендрограммы). Модель k_means: формирование вектора кластеров
в имеющейся выборке - кластеризация клиентов. Статистика и анализ по средним арифметическим значениям признаков по каждому кластеру. Сравнение факторов риска оттока, 
определенных вручную, и признаков, выявленных с помощью машинного моделирования. Визуализация распределения признаков для самого "бросающего" и самого "надежного" кластера.
### Результаты
* "Вручную" выделили признаки клиента фитнеса, коррелирующие с последующим оттоком.
* Обучили две модели прогнозирования оттока на имеющихся данных, оценили их точность.
* Определили число кластеров и разделили клиентов на кластеры. Выделили один самый "бросающий" кластер, остальные приняли как "надежные".
* Сделали вывод о факторах риска оттока на основе результатов машинного обучения.
* Разработали базовые рекомендации по профилактике оттока среди клиентов для менеджеров фитнес-сети.
### Статус проекта
+ Завершен.