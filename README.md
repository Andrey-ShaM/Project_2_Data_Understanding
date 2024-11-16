# Проект 1. Анализ данных

## Оглавление

[1. Описание проекта](#описание-проекта)

[2. Цель проекта](#цель-проекта)

[3. Краткая информация о данных](https://github.com/Andrey-ShaM/Project_2_Data_Understanding/blob/master/README.md#Краткая-информация-о-данных)

[4. Основные этапы проекта](https://github.com/Andrey-ShaM/Project_2_Data_Understanding/blob/master/README.md#Основные-этапы-проекта)

[5. Результаты](https://github.com/Andrey-ShaM/Project_2_Data_Understanding/blob/master/README.md#Результаты)

[6. Выводы](https://github.com/Andrey-ShaM/Project_2_Data_Understanding/blob/master/README.md#Выводы)

### Описание проекта

В нашем распоряжении будет база данных о вакансиях. 

Мы будем проводить Data Understanding, или анализ данных, как один из этапов работы над ML-проектом.

:arrow_up:[к оглавлению](https://github.com/Andrey-ShaM/Project_2_Data_Understanding/blob/master/README.md#Оглавление)

### Цель проекта

Анализ данных посредством запросов к базам данных с использованием SQL

:arrow_up:[к оглавлению](https://github.com/Andrey-ShaM/Project_2_Data_Understanding/blob/master/README.md#Оглавление)

### Краткая информация о данных

При работе над проектом были использонаны следующие данные:

1. Таблица с данными о вакансиях - vacancies

2. Таблица-справочник, которая хранит код региона и его название - areas

3. Таблица-справочник со списком работодателей - employers

4. Таблица-справочник вариантов сфер деятельности работодателей - industries

5. Дополнительная таблица, которая существует для организации связи между работодателями и сферами их деятельности - employers_industries

6. Непосредственно сам файл с кодом обработки данных SkillFactory_Project_2.ipynb 

7. Используемые версии библиотек приведены в файле requirements.txt

:arrow_up:[к оглавлению](https://github.com/Andrey-ShaM/Project_2_Data_Understanding/blob/master/README.md#Оглавление)

### Основные этапы проекта

Проект состоит из пяти частей:

* Предварительный анализ данных

* Детальный анализ вакансий

* Анализ работодателей

* Предметный анализ

* Дополнительные исследования данных

:arrow_up:[к оглавлению](https://github.com/Andrey-ShaM/Project_2_Data_Understanding/blob/master/README.md#Оглавление)

### Результаты

1. В ходе предварительного анализа данных были полученны следующие результаты:
   * В таблице vacancies представленно 49197 записей (строк) о вакансиях. Столбцы key_skills, salary_from и salary_to имеют пропуски. Количество уникальных названий вакансий (столбец name) составляет 21223.
   * В таблице employers представленно 23501 записей о работадателях. Количество уникальных названий работадателей (столбец name) составляет 23175.
   * В таблице araes представленно 1362 записей о регионах.
   * В таблице industries представленно 294 записей о сферах деятельности работадателей.

2. В ходе детального анализа вакансий были полученны следующие результаты:
   * Топ пять регионов по количеству вакансий (по убыванию) следующий: Москва,Санкт-Петербург, Минск, Новосибирск, Алматы
   * У 24073 записей в таблице с вакансиями заполнено хотя бы одно из полей с зарплатой, что составляет менее 50 %.
   * Среднее значение нижней границы зарплатной вилки составляет 71065 руб, верхней границы - 110537 руб.
   * Второе по численности вакансий сочетание типа рабочего графика (schedule) и типа трудоустройства (employment) является - "Удалённая работа — Полная занятость"
   * Требуемый опыт работы по количеству вакансий (в порядке возрастания) представляет собой следующую последовательность: Более 6 лет — Нет опыта — От 3 до 6 лет — От 1 года до 3 лет
   * В ходе этапа разведывательного анализа были расмотрены следющие распределения и зависимости:   

3. В ходе анализа работодателей были полученны следующие результаты:

   * Топ пять работадателей по количеству вакансий возлавляет Яндекс, а замыкает Газпром нефть.
   * Регион с наибольшим количеством работадателей, при отсутствии вакансий (очевидно, по причине отсутствия указания именно такого названия региона) является Россия.
   * Работадатель с наибольшим количеством регионов, где он размещает свои вакансии - Яндекс, количество регионов - 181.
   * У 8419 работадателей не указана сфера деятельности.
   * Третья по алфавиту компания с четырьмя сферами деятельности - 2ГИС.
   * В качестве сферы деятельности указана «Разработка программного обеспечения» у 3553 работадателей.
   * Яндекс представляет вакансии во всех 16 городах-миллионниках России, с общим колчеством вакансий по этим городам - 485.

4. В ходе предметного анализа были полученны следующие результаты:
   * Среди всех вакансий 1771 имеют отношение к данным, в её названии содержатся слова 'data' или 'данн'.
   * Количество вакансий для начинающего дата-сайентиста (DS) составляет 51.
   * Количество вакансий для DS, в которых в качестве ключевого навыка указан SQL или postgres, составляет 229.
   * Количество вакансий для DS, в которых в качестве ключевого навыка указан Python, составляет 357.
   * В среднем в вакансиях для DS указывают 6.41 ключевых навыков.
   * В среднем в вакансиях для DS с опытом работы от 3 до 6 лет указывают зарплату в 243115 руб.

5. В ходе дополнительного анализа были полученны следующие результаты:
   * Тройка самых распространенных сфер деятельности - "Разработка программного обеспечения" (12499 вакансии), "Системная интеграция, автоматизации технологических и бизнес-процессов предприятия, ИТ-консалтинг" (11034 вакансии), "Интернет-компания (поисковики, платежные системы, соц.сети, информационно-познавательные и развлекательные ресурсы, продвижение сайтов и прочее)" (6413 вакансии)
   * Дата-саентист наиболее востребован в следующих трёх сферах деятельности: "Разработка программного обеспечения" (148 вакансий), "Системная интеграция, автоматизации технологических и бизнес-процессов предприятия, ИТ-консалтинг" (139 вакансий) и "Банк" (92 вакансии).


В результате работы над проектом была проанализированна, преобразованна и очищенна база данных результат записан в файл data_clean.csv, сохранненый в папке data.

:arrow_up:[к оглавлению](#Оглавление)


### Выводы
1. Данные представлены в 5 таблицах. Основная таблица - vacancies содержит 49197 записей о вакансиях. Три таблицы-справочника - areas (1392 записи), employers (23501 запись) и industries (294 записи), содержащие информацию о регионе, работадателе и сфере деятельности соответственно. И одна дополнительная таблица - employers_industries для организации связи между работодателями и сферами их деятельности. Практически все представленные данные относятся к категориальным, кроме двух столбцов - salary_from и salary_to.
2. В ходе детального анализа данных выявили, что в таблице vacancies имеется большое количество пропусков в столбцах salary_from и salary_to - только у 24073 вакансий заполнено хотя бы одно из этих полей. А это менее 50 % от полного количества вакансий. Следовательно потребуется дополнительная работа по заполнению пропусков, а также по исключению выбросов.
3. Определили распределение количества вакансий по сочетанию типа рабочего графика (schedule) и типа трудоустройства (employment), по требуемому опыту работы, по работадателю и региону.
4. Определели распределение работадателей по регионам.
5. Рассмотрели сферы деятельности работадателей: у 8419 работадателей сфера деятельности не указана, а у 3553 работаделей в качестве сферы деятельности указана «Разработка программного обеспечения».
6. Рассмотрели распределение количества вакансий компании Яндекс в городах миллионниках России. Из 16 городов-миллионников, помимо Москвы с 54 вакансиями (11% от общего количества вакансий в городах-миллиониках) и Санкт-Петербурга с 42 вакансиями (> 9%), следуюет выделить города где количество вакансий 30 или больше : Краснодар (30), Воронеж (32), Новосибирск (35), Нижний Новгород (36) и Екатеринбург (39). В остальных городах количество вакансий распределено довольно равномерно и в среднем составляет примерно 24 вакансии.
7. Из всех представленных вакансий только 1771 имеет отношение к данным. 
8. В ходе предметного анализа провели исследование на предмет количества вакансий, требований к ключевым навыкам, а также определили среднее значение зарплаты для дата-саентиста.
9. Дополнительно было рассмотрено распределение вакансий по сферам деятельности, в том числе рассмотрено в каких сферах наиболее востребована вакансия дата-саентиста.


:arrow_up:[к оглавлению](#Оглавление)