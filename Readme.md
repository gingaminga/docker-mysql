# Docker with MySQL

Docker compose를 통한 MySQL 실행

## 준비하기

```bash
$ git clone https://github.com/gingaminga/docker-mysql.git
$ cd docker-mysql
```

### .env

**.env.sample** 파일은 해당 환경변수들에 대한 설명이 작성되어 있습니다.
참고하여 **.env** 파일을 만듭니다.

```bash
$ vi .env
```

> 🚨 MySQL의 다른 환경변수를 사용하고 싶다면 [Docker MySQL](https://hub.docker.com/_/mysql) 에서 `Environment Variables` 를 확인하세요.

### my.cnf

my.cnf 파일은 MySQL의 초기 설정 파일입니다. (v8.0.31 기준)
.env 파일의 `MYSQL_DEFAULT_CONFIG_FILE` 에 설정해둔 **경로**와 **파일명**에 맞도록 이동시킵니다. (파일 마운트를 위해 해당 방식을 사용합니다.)

## 실행하기

전부 완료됐다면 실행만 하면 됩니다!

```bash
docker compose up -d
```

## 확인하기

### Docker 프로세스 확인하기

```bash
$ docker ps
```

![image](https://user-images.githubusercontent.com/60294629/210055949-a721c6a8-8647-4cb5-9480-fb474dc6edb2.png)

---

### DB 접속 확인하기

MySQL workbench나 HeidiSQL 등 client tool이 있다면, 쉽게 접속해서 확인 가능합니다.

![image](https://user-images.githubusercontent.com/60294629/210055873-69dc3f9d-cf97-4b04-8fc1-46d2f37f422a.png)

> 💡 더 자세한 설명을 원하시면 [Docker+MySQL 삽질기](https://velog.io/@gingaminga/Docker-%EC%82%BD%EC%A7%88%EA%B8%B0-Docker%EB%A1%9C-MySQL-%EC%8B%A4%ED%96%89%ED%95%98%EA%B8%B0)에서 확인해주세요 :)
