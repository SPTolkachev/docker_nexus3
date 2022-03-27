# docker_nexus3
Docker composition for Nexus 3 by Sonartype.

## Install and run
1. Git clone.
```shell
git clone git@github.com:SPTolkachev/docker_nexus3.git
```

2. Create `docker-compose.yml` from `docker-compose.yml.example`.
```shell
cp docker-compose.yml.example docker-compose.yml
```

3. Create `.env` from `.env.example` and change values.
```shell
~$ cp .env.example .env
~$ nano .env
```

4. Create dir `~/data/` (param `DIR_DATA` from `.env`).
```shell
~$ mkdir data
~$ sudo chmod 777 data
```

5. Pull docker image.
```shell
~$ docker-compose pull
```

6. Run.
```
~$ docker-compose up -d
```

7. Open `HOSTPORT` (initial -- `localhost:8081`) from `.env` in your browser.


## Config .env
- `HOSTPORT` -- nexus' web interface host and port
- `DIR_DATA` -- path to directory of data


## Sign in
1. Copy password from `data/admin.password` (if `DIR_DATA=./data`)
```
~$ cat data/admin.password | xclip -sel clip
```
