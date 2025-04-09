# dockeredmetric
##Dockered Сервис сбора метрик и алертинга <br>
*Курс "Продвинутый Go-разработчик" Yandex Practicum*

Не имел опыта работы с docker-compose, но, вроде бы, сделал файлы для Метрик

Собираются-запускаются 3 контейнера - **База Данных, Сервер и Агент**<br>
Агент собирает runtime-метрики, отсылает их на Сервер, Сервер записывает в Базу Данных

Надеюсь, будет полезно - код несложный, но пришлось повозиться, погуглить<br>
Цель была - научиться писать dockerfile, docker-compose  и чтобы контейнеры видели друг друга и принимали данные

Файлы расположить в корне проекта Метрик

```Metric
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
```
<hr>
Далее

**docker-compose build**<br>
**docker-compose up**

*curl localhost:8000
и прочие курлы*
