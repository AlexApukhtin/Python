Характеристика пользователей интернет-магазина:<br>
<b>Проект завершеню</b><br>
Дан лог с действиями пользователей на сайте.

<b>Цель работы:</b><br>
В интернет-магазине проводится ребрендинг сайта (было решено изменить шрифт у одной из групп пользователей), требуется выяснить , как сказалось данное решение на посещаемости сайта и кол-ве продаж.
Для реализации поекта были использованы базовые библиотеки Python: pandas, seaborn, plotly, numpy,  а также stats для проверки статистических гипотез.

<b>Ход работы:</b><br>
<li>Предоработка данных (обработка названий столбцов, проверка дубликатов, обработка типа данных содержащих время посещения).</li>
<li>Изучение данных (проверка кол-ва пользователей в логе, кол-ва событий, среднего кол-ва событий на пользователя).</li>
<li>Построение гистограммы активности пользователей на сайте, отсечение не полных данных (не все данные за устаревший периодмогут быть отображены в датасете).</li>
<li>Определение числености экспериментальных групп.</li>
<li>Изучение воронки событий, их последовательности и конверсии.</li>
<li>Проведение А/А и А/В тестов. Подбор оптимального коэффициента значимости alpha.</li>
<br>
<b>Выводы:</b><br>
<ol>Воронка продаж определилась следующая: main_screen_appear, offer_screen_appear, card_screen_appear, payment_screen_successful. Событие tutorial необязательное перед покупкой.</ol>
<ol>Больше всего пользователей теряется при переходе из события main_screen_appear в offer_screen_appear: 38.07%.</ol>
<ol>Было выполнено по 12 А/В тестов для каждой событийной группы. Alpha ==0.1 будет слишком высоким, при таком его значении вероятность погрешности 10%, значит как минимум один результат будет ложным при тестировании.</ol>  
