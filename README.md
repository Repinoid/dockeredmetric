# dockeredmetric
Dockered Сервис сбора метрик и алертинга. Продвинутый Go-разработчик Yandex Practicum

Не имел опыта работы с docker-compose, но, вроде бы, сделал файлы для Метрик

Собираются-запускаются 3 контейнера - База Данных, Сервер и Агент
Агент собирает runtime-метрики, отсылает их на Сервер, Сервер записывает в Базу Данных

Надеюсь, будет полезно - код несложный, но пришлось повозиться, погуглить
Цель была - научиться писать dockerfile, docker-compose  и чтобы контейнеры видели друг друга и принимали данные

Файлы расположить в корне проекта Метрик
(чтобы увидеть схему, откройте README.md, переключитесь в режим CODE)

Metric
├─ cmd
|   ├── server
|   |     ├── server.go
|   |     └── *.go
|   └── agent
|         ├── agent.go
|         └── *.go
├─ internal
|   └── *
|       └── *.go
|
├─ docker-compose.yml
├─ AgentDockerFile
└─ ServerDockerFile


Далее

docker-compose build
docker-compose up

curl localhost:8000
и прочие курлы
