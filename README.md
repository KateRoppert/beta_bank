# beta_bank
Из «Бета-Банка» стали уходить клиенты. Каждый месяц. Немного, но заметно. Банковские маркетологи посчитали: сохранять текущих клиентов дешевле, чем привлекать новых.

Нужно спрогнозировать, уйдёт клиент из банка в ближайшее время или нет. нам предоставлены исторические данные о поведении клиентов и расторжении договоров с банком.

Задача: построить модель с предельно большим значением F1-меры (минимум 0.59). Проверить F1-меру на тестовой выборке. Дополнительно измерять AUC-ROC, сравнивая её значение с F1-мерой.

Источник данных: https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling

Были исследованы три модели: решающее дерево, логистическая регрессия и случайный лес. Использованы три техники перебалансировки классов: взвешивание классов, upsampling, downsampling.

В результате была выбрана модель случайного леса, показавшая наилучшие результаты, с характеристиками:
Метрика AUC-ROC: 0.85. Лучше, чем у случайной модели, логистической регрессии и решающего дерева.
Лучший результат модели случайного леса: 0.6
Перебалансировка: upsampling
Порог: 0.48
