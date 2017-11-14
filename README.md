# docker-rneo4j

example on how to use [neo4j](https://neo4j.com/) with r using [RNeo4j](https://github.com/nicolewhite/RNeo4j)

## pull

```bash
$ docker pull crazycapivara/rneo4j
```

## or build

```bash
$ docker build -t crazycapivara/rneo4j .
```

## run

```bash
$ docker-compose up
```

- docker-compose spins up a neo4j database and an r terminal container
- a helper scripts checks every 2 seconds whether the database is up and inserts data when the database ready
- afterwards you can play around with the data in the neo4j web gui

## browse

http://localhost:7474 (see `docker-compose.yml` for uid and pwd)

run some query in the web gui ...

```bash
MATCH (n) -[:IMPORTS]-> (dep {name: "Rcpp"}) RETURN n,  dep
```

