Тестовое задание №1

SELECT
	task_info.issue_key AS issue_key
	task_info.name AS name
	task_info.type AS type
FROM
	task_info
INNER JOIN task_status ON task_status.issue_key = task_info.issue_key
WHERE
	task_info.type = 'Bug' AND
	task_status.status = 'in progress' AND
	task_status.start_time >= '2021-04-01' AND
	task_status.start_time < '2021-05-01'


Тестовое задание №2

Название класса	        Тип класса	Границы	        Тестовые данные внутри класса   	Тестовые данные на границах	Пояснение
                                                        
0 - 99 баллов	        диапазон	0, 99	                       5	                            0, 1, 98, 99	1% скидки
100 - 199 баллов	диапазон	100, 199	              105	                      100, 101, 198, 199	3% скидки
200 - 499 баллов	диапазон	200, 499	              205	                      200, 201, 498, 499	5% скидки
500 - бесконечность	диапазон	500	                      505	                                500, 501	10% скидки
