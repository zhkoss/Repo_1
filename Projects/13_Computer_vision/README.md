# Определение возраста покупателей

Определение возраста покупателей по фотографиям с помощью библиотеки Keras и нейросети ResNET50.<br>

## Анализ обученной модели
В данном проекте с целью определения возраста покупателей в качестве основной (backbone) была использована нейрость ReNet50 с весами датасета ImageNet.

Использован 1 полносвязный слой (большее количество слоев в (т.ч. BatchNormalization) ухудшало качество модели).
В модели не использовалось замораживание ResNet50 без верхушки (т.к. это давало худший результат). В качестве целевой метрики использована MAE.

За 9 эпох и c применением алгоритма Adam удалось достичь метрики MAE на тестовой выборке со значением 6.591. С большой долей вероятности тренировочную и тестовую метрики можно улучшить, увеличивая количество эпох, а также проводя дополнительные аугментации исходных изображений.

## Что использовано
Python, Numpy, Pandas, Matplotlib, Seaborn, Tensorflow.keras.
