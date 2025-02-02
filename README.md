# mlops2

## Состав команды:
Кравцов Артем (РИМ-120907)  
Саенко Лев (РИМ-120906)  
Лихачев Денис (РИМ-120906)  
Коломенский Виктор (РИМ-120907)  

# Задание 4

Весь исходный код для выполнения находится в основном репозитории https://github.com/Basserti/mlops

# Задание 1

## Настройка окружения
Все необходимые зависимости прописаны в файле requirements.txt

## Этапы:

1.	Python-скрипт data_creation.py генерирует данные по температуре за 10 лет с добавлением к ним шума. 
9 из них сохраняется по пути 'train/train.csv', оставшийся год - 'test/test.csv'.

![image](https://user-images.githubusercontent.com/26464655/221661738-990dfcff-b503-4b87-a059-658be485e468.png)

2.	Python-скрипт model_preprocessing.py предобрабатывает данные для обучения при помощи sklearn.preprocessing.RobustScaler. Далее сохраняет предобработанный файл train по пути 'train/train_preprocessing.csv'. Также сохраняется скалер для дальнейшей предобработки тестового набора данных.

3.	Python-скрипт model_preparation.py обучает модель Prophet на данных из файла 'train_preprocessing.csv' и сохраняет её в корневую директорию.

4.	Python-скрипт model_testing.py загружает тестовые данные, подготавливает их скалером и делает предсказания предобученной моделью. Происходит расчет метрики MAE и вывод результата в консоль.

5.	Bash-скрипт pipeline.sh последовательно запускает все python-скрипты.
