# Проект для «Викишоп» с BERT

[HTML](https://github.com/lodygin-mikhail/yandex-practicum-data-scientist/blob/main/Text%20analysis/Project%208.html)     [ipynb](https://github.com/lodygin-mikhail/yandex-practicum-data-scientist/blob/main/Text%20analysis/Project%208.ipynb)

## Описание проекта
Интернет-магазин «Викишоп» запускает новый сервис. Теперь пользователи могут редактировать и дополнять описания товаров, как в вики-сообществах. То есть клиенты предлагают свои правки и комментируют изменения других. Магазину нужен инструмент, который будет искать токсичные комментарии и отправлять их на модерацию. 

Обучите модель классифицировать комментарии на позитивные и негативные. В вашем распоряжении набор данных с разметкой о токсичности правок.

Постройте модель со значением метрики качества *F1* не меньше 0.75. 


## Навыки и инструменты

- pandas
- numpy
- scikit-learn
- seaborn
- transformers
- Random Forest
- LightGBM

## Общий вывод
С помощью полученных от заказчика данных был разработан инструмент для определения токсичных комментариев. 

Для это была использована языковая модель toxic_Bert из открытого доступа. С помощью данной модели были получены CLS-токены комменариев. 

В проекте были обучены три модели на кросс-валидации:
- Логистическая регрессия
- Случайный лес
- LightGBM

Лучший результат при кросс-валидации показала модель **RandomForestClassifier** (F1 метрика равна **0,934**), на тестовых данных ее результат **0,943**.

Таким образом, была построена модель со значением метрики качества F1 более 0.75 для интернет-магазина «Викишоп».
