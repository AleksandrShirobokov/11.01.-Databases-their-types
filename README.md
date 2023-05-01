# 11.01.-Databases-their-types
# Александр Широбоков

## Задание 1. СУБД
 - 1.1. Для бюджетирования проектов и формирования финансовых аналитических отчетов лучше всего использовать реляционные СУБД, такие как PostgreSQL, Oracle или Microsoft SQL Server. Они обеспечивают целостность и четкую структуру данных, что особенно важно для финансовых данных. Для прогнозирования рисков можно использовать алгоритмы машинного обучения, например, в Python с библиотеками Pandas, NumPy и Scikit-learn.

*1.1. Для ускорения работы хеширования можно использовать более быстрые алгоритмы, такие как SHA-256 или BLAKE2, а также использовать параллельную обработку или аппаратное ускорение (например, GPU или ASIC).*

 - 1.2. Для лендингов и CRM лучше использовать NoSQL СУБД, такие как MongoDB или Cassandra. Они более гибкие и могут быстрее обрабатывать большие объемы неструктурированных данных, таких как лиды и информация о клиентах. Можно использовать одну СУБД для лендингов и CRM, например, MongoDB, которая хранит неструктурированные данные в формате BSON и может быстро обрабатывать запросы на поиск и фильтрацию данных.

*1.2. Да, эту задачу можно решить одной СУБД, например, MongoDB. Она обеспечивает гибкость и быстродействие для хранения данных лендингов и CRM, а также позволяет быстро обрабатывать запросы на поиск и фильтрацию данных.*

 - 1.3. Для создания базы по корпоративным нормам и правилам лучше всего использовать реляционные СУБД, такие как PostgreSQL или Microsoft SQL Server. Они обеспечивают простую и понятную структуру данных, что особенно важно для организации информации о корпоративных нормах и правилах.

*1.3. Да, можно использовать уже существующую СУБД, например, PostgreSQL или Microsoft SQL Server, и создать новую таблицу для хранения информации о корпоративных нормах и правилах. Это позволит использовать уже существующую инфраструктуру и обеспечит целостность данных.*

 - 1.4. Для решения задач логистики, связанных с формированием маршрутов доставки материалов и распределением курьеров по маршрутам, лучше всего использовать графовые СУБД, такие как Neo4j или OrientDB. Они обеспечивают быстрое выполнение запросов и работу со связями между данными, что важно для решения задач логистики.

*1.4. Конечно, можно подключить отдел закупок к СУБД логистов, особенно если эти отделы тесно взаимодействуют между собой. В таком случае, рекомендуется использовать реляционную СУБД, которая позволяет работать со связанными данными и поддерживать транзакции.*

*1.5. Возможно, все задачи можно решить, используя одну СУБД, если она позволяет работать с различными моделями данных, такими как реляционная, графовая, документоориентированная и т.д. Например, MongoDB является документоориентированной СУБД, которая также поддерживает графовую модель данных. Однако, следует учитывать, что такой подход может усложнить структуру базы данных и увеличить нагрузку на её производительность. Поэтому, для решения разных задач может потребоваться использование разных типов СУБД.*

## Задание 2. Транзакции
2.1. Для успешного завершения транзакции по пополнению баланса счёта телефона должны произойти следующие шаги:

 - Пользователь вводит сумму пополнения и подтверждает операцию.
 - Система проверяет наличие достаточного количества денег на счёте пользователя или наличие установленного лимита кредитования.
 - Если проверка проходит успешно, система блокирует указанную сумму на счёте пользователя или на кредитной линии.
 - Система формирует транзакцию и отправляет её на обработку в платёжную систему.
 - Платёжная система проверяет транзакцию на наличие ошибок и отправляет запрос на списание указанной суммы со счёта пользователя или кредитной линии.
 - Если списание прошло успешно, система разблокирует заблокированные средства на счёте пользователя или на кредитной линии.

2.1.* Если пополнение счёта телефона происходило бы через автоплатёж, то процедура транзакции была бы следующей:

 - На определённую дату, установленную пользователем, система автоматически генерирует транзакцию на пополнение баланса.
 - Система проверяет наличие достаточного количества денег на счёте пользователя или наличие установленного лимита кредитования.
 - Если проверка проходит успешно, система блокирует указанную сумму на счёте пользователя или на кредитной линии.
 - Система формирует транзакцию и отправляет её на обработку в платёжную систему.
 - Платёжная система проверяет транзакцию на наличие ошибок и отправляет запрос на списание указанной суммы со счёта пользователя или кредитной линии.
 - Если списание прошло успешно, система разблокирует заблокированные средства на счёте пользователя или на кредитной линии.

Основное отличие сводится к первому пункту.

## Задание 3. SQL vs NoSQL
Преимущества SQL-систем по отношению к NoSQL:

 - Структурированные данные: SQL-системы предназначены для работы с реляционными базами данных, что обеспечивает структурированное хранение и обработку данных. В отличие от NoSQL, где данные могут храниться в неструктурированном формате.

 - Гибкость запросов: SQL-системы позволяют создавать сложные запросы для выборки данных, которые могут быть очень гибкими и настраиваемыми. В NoSQL же запросы могут быть ограничены и не настолько гибкими, как в SQL.

 - ACID-транзакции: SQL-системы предоставляют ACID-транзакции, что гарантирует сохранность и целостность данных. Это особенно важно для критических приложений, где данные должны быть доступными и сохраненными в любых условиях.

 - Высокая производительность: SQL-системы способны работать с большими объемами данных и обеспечивать высокую производительность запросов. Некоторые NoSQL-системы, например, MongoDB, также могут работать с большими объемами данных, но производительность SQL-систем в целом выше.

 - Масштабируемость: SQL-системы могут масштабироваться вертикально и горизонтально, обеспечивая высокую доступность и расширяемость. Некоторые NoSQL-системы также могут масштабироваться, но SQL-системы в целом более гибки и масштабируемы.

Преимущества NewSQL систем перед SQL и NoSQL:

 - Сочетание преимуществ SQL и NoSQL: NewSQL системы обеспечивают сочетание преимуществ SQL и NoSQL, что позволяет использовать реляционную модель данных вместе с гибкостью NoSQL.

 - Высокая производительность: NewSQL системы предназначены для работы с большими объемами данных и обеспечивают высокую производительность запросов, как SQL-системы.

 - ACID-транзакции: NewSQL системы поддерживают ACID-транзакции, как SQL-системы, что гарантирует сохранность и целостность данных.

 - Масштабируемость: NewSQL системы обеспечивают горизонтальное масштабирование и высокую доступность, как SQL-системы.

 - Поддержка больших данных: NewSQL

## Задание 4. Кластеры
При выборе СУБД для обработки больших объёмов данных и распределённых вычислений, ключевым критерием является возможность обеспечения высокой производительности и масштабируемости системы. Для этой задачи необходимо выбрать СУБД, которая может распределять нагрузку на несколько серверов и обеспечивать быстрый доступ к данным.

Для обработки больших объёмов данных в распределённой среде, наиболее подходящей моделью является модель shared-nothing, в которой каждый узел кластера работает автономно и обрабатывает свою часть данных. При этом, для эффективной обработки большого количества запросов, необходимо использовать параллельные алгоритмы и распределённую обработку запросов.

Одной из самых популярных СУБД для обработки больших объёмов данных в распределённой среде является Apache Cassandra. Она использует модель распределения данных типа peer-to-peer, где каждый узел кластера равноправен и не зависит от других. Основными преимуществами Apache Cassandra являются масштабируемость, производительность и отказоустойчивость. Ещё одной популярной СУБД для обработки больших объёмов данных в распределённой среде является Apache Hadoop, который также основан на модели распределения данных типа shared-nothing и поддерживает распараллеливание запросов.

Также стоит упомянуть о NewSQL СУБД, которые сочетают в себе преимущества SQL и NoSQL систем. Они обеспечивают горизонтальную масштабируемость и высокую производительность при обработке большого количества транзакций и запросов на чтение и запись.

 - При выборе типа СУБД для обработки большого объема данных на 1000 машинах следует руководствоваться критериями масштабируемости, производительности, надежности и возможностей распределенных вычислений. Среди типов СУБД, наиболее подходящим для данной задачи будет распределенная СУБД, способная работать с кластером серверов, так как она позволяет балансировать нагрузку на каждом сервере, обеспечивая высокую производительность и надежность работы. В данном случае, рекомендуется использовать модель распределенных вычислений shared-nothing, так как она предполагает, что каждый узел кластера работает автономно и не зависит от других узлов, что позволяет более эффективно масштабировать кластер и обрабатывать большие объемы данных. Таким образом, для данной задачи рекомендуется выбрать распределенную СУБД с моделью shared-nothing, такую как Apache Cassandra, Hadoop Distributed File System (HDFS) или Google Bigtable, которые обеспечивают высокую производительность, масштабируемость и надежность при работе с большими объемами данных в кластере из 1000 машин.
