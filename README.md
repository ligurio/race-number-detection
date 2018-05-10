Каждый раз после соревнования возникает одна и та же проблемы: у участника
соревнования - найти фотографии, на которых он присутствует, у фотографов -
найти спортсменов, которые попал в кадр его фотоаппарата. В случае решения этих
проблем фотографии могут быть как доступны бесплатно для участников так и за
разумную плату. Но нас интересует именно технология, способствующая решению
обоих задач, поэтом коммерческую составляющую в случае решения этих задач мы
оставим за рамками нашего проекта.  Очевидно, что для решения обоих задач нужно
каким-то образом идентифицировать участникаов соревнования на каждой из
фотографий и сделать это можно если вы знаете человека лично ("узнаете его в
лицо") или можете прочитать номер участника на фотографии.  Для первого случая
вы должны знать всех участников, что для крупных соревнований маловероятно, или
иметь достаточно свободного времени, чтобы посмотреть на каждую фотографию и
для каждой из них подготовить список номер участников на этой фотографии.  Есть
предположение, что для второго случая возможно решение с помощью машинного
обучения. Если получится сделать технологию с распознаванием номеров с
вероятность выше 50%, то можно будет подумать создании коммерческого сервиса.


### How-To Use:

- скачать csv с https://requester.mturk.com/
- проревьюить качество аннотаций ```mturk-csv-review.py```
- удалить старый набор данных ```rm -rf data/race_numbers```
- установить модули: ```pip install -r requirement.txt```
- подготовить набор данных и аннотацию ```bib_prepare_dataset.py```
- обучение на наборе данных MNIST - ```bib_learn_mnist.py```
- обучение на реальных изображениях ```bib_learn_custom_dataset.py```
- использование ```bib_predict.py sample.jpg```

Copyright 2018 Sergey Bronnikov
