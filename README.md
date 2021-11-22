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
$ git clone https://github.com/fimochka-sudo/GB_docker_flask_example.git
$ cd GB_docker_flask_example
$ docker build -t course_proj_rest_api .
# Запускаем контейнер
Здесь Вам нужно создать каталог локально и сохранить туда предобученную модель (<your_local_path_to_pretrained_models> нужно заменить на полный путь к этому каталогу)

$ docker run -d -p 8180:8180 -p -v <your_local_path_to_pretrained_models>:/app/app/models fimochka/gb_docker_flask_example
# Переходим на localhost:8181
