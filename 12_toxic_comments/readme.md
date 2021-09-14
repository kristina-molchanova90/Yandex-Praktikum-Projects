**Проект "Поиск токсичных комментариев"**<br>
Построоить модель, классифицирующую комментарии на позитивные и негативные на основании набора данных с разметкой о токсичности правок (*F1* не меньше 0.75)<br><br>
**Используемые библиотеки**<br>
pandas, numpy,  sklearn.feature_extraction, nltk.stem, nltk.corpus, sklearn.linear_model, lightgbm, sklearn.model_selection, sklearn.metrics, matplotlib.pyplot, wordcloud

**Вывод**<br>
Текст очищен от ненужных символов и лемматизирован, создан счетчик TF-IDF и корпус слов (для обучающей и тестовой выборки). Обучены следующие модели, давшие следующие результаты:

| model_name                  | train_score (F1) | test_score (F1) |
|-----------------------------|------------------|-----------------|
| DummyClassifier             | 0.184593         | 0.184578        |
| LogisticRegression balanced | 0.830707         | 0.732107        |
| SGDClassifier balanced      | 0.76632          | 0.720483        |
| LGBMClassifier balanced     | 0.843972         | 0.751486        |

Как можно видеть, качество абсолютно всех рассмотренных моделей намного выше, чем у dummyclassifier. Наиболее низкая степень переобучения -у SGDClassifier, однако у LogisticRegression и LGBMClassifier качество несколько выше. При этом у LGBMClassifier степень переобучения заметно ниже, чем у логистической регрессии. Это говорит о том, что среди рассмотренных моделей LGBMClassifier - наиболее корректно работающая модель
