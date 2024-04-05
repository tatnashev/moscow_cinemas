# Советский кинопрокат
Проект про советский кинопрокат

## О чем проект? 
Советский кинопрокат - проект, рассказывающий об особенностях советского кинопроката на стыке двух периодов - тоталитарном контроле в сталинскую эпоху и начале Оттепели. Начавшись с вопроса "а что такое разряды кинотеатров?", проект в итоге вылился в большое исследование, рассказывающее о московских кинотеатрах того времени, советских и зарубежных фильмах, цензуре и наградах на основе собранных данных.

## Данные 
Все данные хранятся в репозитории проекта в папке `data`, большая часть сохранена в формате `csv/xlsx`. Следующие файлы являются наиболее важными для проекта: 
* `Cinemas_Moscow_1946-1955` - исходные данные, собранные и переданные нам нашим куратором - Кристиной Танис. Содержат детальную информацию по каждому кинотеатру; 
* `moscow_cinemas` - также исходные данные от куратора, содержат информацию по кинопрокату - в каком кинотеатре показывали, первый день показа, количество дней в прокате, название, IMDb ID
* `премии фильмов` - датасет о наградах/цензурировании фильмов за оба периода, собранный Екатериной Неделяевой
movies_final_version - информация о фильмах (рейтинг, жанр, режиссер), которая была взята с IMDb по IMDb ID из файла moscow_cinemas 
* `agg_stat_first_period` - агрегированная статистика, составленная на основе двух исходных датасетов, за первый период 
* `agg_stat_second_period` - агрегированная статистика, составленная на основе двух исходных датасетов, за второй период
* `Cinemas_for_geojson` - файл для визуализации кинотеатров на карте

## Код 
Небольшое описание кода в данном репозитории: 
* `movies_information_parsing` - код для парсинга данных с IMDb по IMDb ID
* `movies_information_processing` - код формирование агрегированного датасета за каждый период
* `visualization_and_more_analysis` - EDA агрегированных датасетов с большим количеством различных визуализаций, обучение различных моделей, где целевая переменная - разряд кинотеатра, анализ работы полученных моделей, поиск кинотеатров-выбросов

В данном репозитории также существует вторая ветка - `project`, в которой содержится попытка рефакторинга получившегося кода, однако туда перенесен не весь функционал. 
