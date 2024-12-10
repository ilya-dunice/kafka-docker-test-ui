>https://habr.com/ru/articles/753398/

* Теперь давайте добавим нашу kafka в kafka-ui. Для этого давайте нажмем на кнопку configure new cluster где вам нужно заполнить следующие поля:
    1. Cluster name - Можете указать просто как "Kafka Cluster"
    2. Bootstrap Servers - Суда вам внужно вписать PLAINTEXT://kafka:29092 (У меня там 2 поля(под урл и под порт): URL:"PLAINTEXT://kafka" PORT:"29092") ну или другое наименование в зависимости от вашей конфигурации параметра "KAFKA_ADVERTISED_LISTENERS" в kafka image. Соотвественно если у вас поднято несколько реплик кафки, вам нужно их всех вписать. Apache рекомендуют иметь 3 ноды с kafka на вашем проекте.
    3. Metrics
        1. metrics type -> JMX
        2. port -> 9997 ну или как вы указали в своей конфигурации