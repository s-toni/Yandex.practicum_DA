# Проект по оценки корректности A/B тестирования

### Цель исследования:

Оценить корректность проведения теста и проанализируйте его результаты. Проверить исполнение технического задания

#### Навыки и инструменты:
 А/В-тестирование, проверка статистических гипотез, метод Бонферрони
- python
- pandas
- seaborn
- matplotlib
- plotly
- scipy
- math
- datetime
- А/В-тестирование
- проверка статистических гипотез
- метод Бонферрони

#### Итоги проведения А/В-теста:

В ходе проведения исследовательского анализа было выявлено следующее:
- Всплеск активности происходит в период с 15.12 по 23.12 с пиком на 22.12, что вполне логично, т.к. тест проводиться для Европы и пользователи готовятся к Рождественским праздникам.
- Большинство пользователей совершают первые действие в первый день после регистрации независимо от группы теста.
- В среднем пользователь группы А совершает событий больше (почти 7 событий), чем пользователи группы В (5,5), медианное значение также выше - 6 против 4. Максимальное количество событий пользователей обеих групп равно 24.
- Распределение по устройствам группы А также сильно выше.
- При исследовании воронки событий было определено 4 события - самое популярное событие - регистрация (почти 100%), далее идет просмотр страницы (63%). После логина до страницы с оплатой доходят 31% пользователей. Интересным является факт, что покупка имеет больший процент посещения, чем просмотр корзины (29%). 

<div style="text-align: justify ">
По итогам проверки проведенного А/В-теста можно сделать вывод, что экспериментальная группа не достигла поставленной цели по улучшению каждой метрики не менее, чем на 10%. При проведение z-теста было отмечено, что статистически значимых различий между событиями групп А и В по трем действиям не наблюдается. Значимые различия между долями групп А и В имеются только по событию просмотр страницы товара. Таким образом результаты проведенного тестирования можно считать не удовлетворительными, поставленные цели достигнуты не были.<br>
Важно отметить, что период проведения теста выбран крайне неудачным, т.к. это время подготовки к Рождеству. Кроме того даты окончания теста не соответствуют заявленным в ТЗ датам. Желаемый процент новых пользователей из Европы - 8,22%, что почти в 2 раза меньше заявленной в ТЗ (15%). Ожидаемое количество участников также сильно ниже ожидаемых - чуть более 3,5 тыс. пользователей. Разница между количеством пользователей групп достаточно большая. Кроме того, во время прохождения теста проходила рождественская акция. Также параллельно проходил еще один тест. Все эти факторы могли сказаться на результатах проведения А/В-теста.
</div><br>

### Вывод:
в ходе проведения исследования была проведена оценка корректности A/B тестирования. Проверено исполнение Технического задания, подведены итоги А/В-теста.

<b>Примечание:</b> в проекте при построении воронки событий была использована библиотека plotly, которай не позволяют отображать результат кода на GitHub. По данной причине такой код и графики были вставлены скриншотом.
