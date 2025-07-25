
# Overview

Данное соревнование - финальный проект в рамках интенсива по машинному обучению Академии Яндекса (сезон осень 2024).

# Description

В этом соревновании нужно написать свёрточную нейронную сеть для классификации изображений.

Вам предоставлен датасет с фотографиями людей, занятых различными активностями:
- sports
- occupation
- conditioning exercise
- home activities
- lawn and garden
- home repair
- water activities
- winter activities
- miscellaneous
- fishing and hunting
- dancing
- walking
- music playing
- bicycling
- running
- inactivity quiet/light

Размер обучающей выборки (train) - 12 тысяч изображений, тестовой выборки (test) - 5 тысяч изображений.

В данном домашнем задании нет никаких ограничений по архитектуре модели, но реализовывать в pytorch/tensorflow её надо самим и обучить с нуля только на данном датасете, без внешних данных.

# Evaluation

Качество решения будет оцениваться по метрике f1-score, чтобы сбалансировать precision и recall:

f1 = (2 * precision * recall) / (precision + recall)

Обратите внимание, что публичный лидерборд рассчитывается по 50% тестовых данных, поэтому старайтесь не переобучаться под него.

# Submission File

В качестве решения вы должны прислать файл формата:
- Id,target_feature
- 0,0
- 1,1
- 2,1
- etc

где Id - порядковый номер объекта в тестовом датасете, target_feature — предсказанный класс объекта.

# Dataset Description
- img_train - изображения из обучающей выборки
- img_test - изображения из тестовой выборки
- train_answers.csv - классы для изображений из обучающей выборки
- activity_categories.csv - соответствие id классов и человекочитаемых активностей

Данные: http://human-pose.mpi-inf.mpg.de/#overview