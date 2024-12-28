#### Проект 2: Анализ продаж сети кофеен в Python

Наша задача — проанализировать распределение продаж по сети, продажи в разрезе категорий продукции, целевую аудиторию кофеен, а также выявить возможные взаимосвязи продаж с имеющимися признаками. Полученные результаты необходимо представить в аналитическом отчете, содержащим выводы и рекомендации для Заказчика, которые помогут ему для решения его бизнес-задач.

Часть 1. Предобработка данных.ipynb

1. Был представлен датасет с выгрузкой о транзакциях, товарах, клиентах и торговых точках из CRM-системы Заказчика. Файл в формате csv, содержащий 24909 строк (объектов) и 6 столбцов (признаков).
2. Предобработка данных включала в себя: исключение нерелевантных признаков и наблюдений, полных дубликатов (ошибочно задвоенных записей), распаковку и форматирование данных, проверку признаков на наличие незаполненных значений, расчет дополнительных признаков.
3. По итогу предобработки сохранен преобразованный датасет для последующего анализа:
* датасет в разрезе уникальных транзакций (24852 объектов, 12 признаков): файл в формате csv (coffee_shop_prepared.csv).

Часть 2. Анализ данных.ipynb  

1. Проведен анализ целевой аудитории и сформирован обобщённый портрет посетителей сети.
* Молодежная аудитория более активно пользуется услугами данной сети кофеен, возможно, благодаря современным трендам и культурным предпочтениям.
* Более зрелые клиенты менее заинтересованы в посещении кофеен, либо предпочитают альтернативные форматы питания и отдыха (снижение интереса с возрастом к подобному формату).
* Можно сделать вывод об отсутствии значимой взаимосвязи между полом и предпочтениями клиентов сети кофеен.
2. Распределение продаж по сети кофеен в разрезе торговых точек.
* Выявлена значительная разница в количестве уникальных клиентов для каждой торговой точки, так на торговой точке № 8 (Москва) кол-во уникальных клиентов - 501 чел, в то время как на торговых точках: № 5 (Москва) - 944 чел, № 3 (СПб) - 800 чел.
При этом кол-во повторных покупок на одного уникального клиента (retention, коэффициент удержания клиентов) на торговой точке № 8 намного выше (на 50%) и составляет 15 ед., чем этот показатель на двух других точках, на №5 - 9 ед., на №3 - 11 ед.
В связи с этим, рекомендуется проанализировать ключевые характеристики торговых точек и выявить возможные причины столь большой разницы в показателях (кол-во уникальных клиентов, retention).
* Распределение выручки по торговым категориям практически одинаково для всех трех торговых точек и совпадает с распределением выручки по торговым категориям в общем по сети. Это может указывать на однородность целевой аудитории на разных торговых точках (схожие предпочтения клиентов), единую маркетинговую стратегию, единую ассортиментную линейку (на всех торговых точках), эффективное управление товарными запасами и т.д.
Несмотря на то, что распределение выручки по торговым категориям практически одинаково для всех трех торговых точек, список ТОП-10 самых популярных (наиболее часто продаваемых) и список LOW-10 самых редко продаваемых товаров, разный для каждой торговой точки и содержит мало пересечений по товарам.
Это может указывать на локальные предпочтения потребителей, адаптацию торговых точек под окружающую их конкурентную среду, корректировки ассортимента под текущие тенденции спроса.

3. Рекомендации.
* Поскольку молодые люди являются основными клиентами сети, это может стать ориентиром для дальнейшего развития текущего бизнеса и при открытии новых торговых точек. В таком случае можно рекомендовать мероприятия, способствующие повышению лояльности молодежной аудитории.
* Следует обратить внимание на категории сопутствующих товаров, т.к. их совокупная доля в общем обьеме продаж (8%) очень мала и отличается от среднестатистической в аналогичных случаях (10-30%). Практические рекомендации по исправлению также были предложены Заказчику.





