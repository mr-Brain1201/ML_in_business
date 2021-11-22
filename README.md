Задача: Предсказать стоимость жилья в индийском городе Ченнай.
Задача регрессии.
Предсказание производится на основании района расположения, застройщика, площади и возраста дома.

Используемые признаки:

'location' (str);
'builder' (str);
'area' (int);
'age' (float)
Преобразования признаков: столбец 'area' через standardscaler

Модель: catboost

# Клонируем репозиторий и создаем образ
```
$ git clone https://github.com/mr-Brain1201/ML_in_business.git
$ cd ML_in_business
$ docker build -t course_proj_rest_api .
```
# Запускаем контейнер
Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)
```
$ docker run -d -p 8180:8180 -v /app/app/models:/app/app/models course_proj_rest_api
```
# Переходим на localhost:8180
