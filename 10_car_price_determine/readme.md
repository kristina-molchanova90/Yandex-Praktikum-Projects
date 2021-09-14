**Проект "Определение стоимости автомобиля"**<br>
Цель - обучить модель для определения стоимости автомобилей. Важные критерии: качество предсказания, скорость предсказания, время обучения<br><br>

**Данные, используемые в проекте**<br>
Исторические данные о ценах автомобилей, технических характеристиках и комплектации<br><br>

**Используемые библиотеки**<br>
pandas, numpy, matplotlib.pyplot ,seaborn, datetime, sklearn.tree, sklearn.ensemble, sklearn.linear_model, sklearn.metrics, sklearn.model_selection, sklearn.preprocessing,lightgbm,catboost

**Вывод**<br>
Были построены следующие модели, давшие следующие результаты:

| model_name        | RMSE Test Data | best Train RMSE | fit time  |
|-------------------|----------------|------------------|-----------|
| DecisionTree      | 1.83E+03       | 1.87E+03         | 4.127833  |
| RandomForest      | 1.70E+03       | 1.69E+03         | 38.663172 |
| Linear Regression | 2.71E+03       | 1.13E+12         | 14.100979 |
| CatBoostRegressor | 1.80E+03       | 1.78E+03         | 6.385439  |
| LGBMRegressor     | 1.62E+03       | 1.61E+03         | 4.39671   |

Как можно видеть, скорость предсказания у модели CatBoostRegressor выше, чем у модели LGBMRegressor, однако у модели LGBMRegressor заметно выше качество и скорость обучения. Поэтому можем рекомендовать ее для определения стоимости автомобилей

Если проект не открывается, его можно посмотреть <a href = "https://nbviewer.jupyter.org/github/kristina-molchanova90/Yandex-Praktikum-Projects/blob/main/10_car_price_determine/10_car_price_determine.ipynb">здесь</a>
