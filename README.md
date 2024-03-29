# Adentis - Scala Exercise

This is a project to study Scala.

## 🚀 Instructions

### 📋 Prerequisite

- Docker (if you don't want install the JDK, Scala and SBT)
- JDK 8+
- Scala 2.13
- SBT 1.5.2

### 🐳 Using Docker
You can run all the Scala/SBT commands described in this README inside a Docker container.

To run and enter inside a docker container just execute:
```shell
 docker run -it --rm -v the/absolute/path/for/the/project/folder/:/app hseeberger/scala-sbt:8u222_1.3.5_2.13.1 bash
```

If you are using Windows:

```shell
docker run -it --rm -v C:\the\absolute\path\for\the\project\folder\:/app hseeberger/scala-sbt:8u222_1.3.5_2.13.1 bash
```

Inside the container, you should enter in the `/app` folder to be able to run the next commands of this README.

### 🔧️ Build and packaging the tool
```shell
sbt compile
sbt package
```

PS.: at first time the `sbt compile` command can take a time

### 🏃 Running the tool

Execute:
```shell
scala target/scala-2.13/adentis-challenge_2.13-0.1.jar "2018-01-01 00:00:00" "2019-01-01 00:00:00"
```

The main arguments (and required) are two dates representing a interval.
So the format of those dates is `year-month-day hours:minutes:seconds` (`YYYY-MM-DD HH:mm:ss`).

You can pass some additional arguments representing the months you want the information will be grouped, like:
```shell
"1-3" "4-6" "7-12" ">12"
```

A full example:
```shell
 scala target/scala-2.13/adentis-challenge_2.13-0.1.jar "2018-01-01 00:00:00" "2019-01-01 00:00:00" "1-3" "4-6" "7-12" ">12"
```

The result should be something like:
```shell
Result:

1-3 months: 200 orders

4-6 months: 150 orders

7-12 months: 50 orders

>12 months: 20 orders
```

You can yet run using IntelliJ IDEA, the tool was made with it.

## ⚙️Executing tests

```shell
sbt test
```

The result should be like:

![image](https://user-images.githubusercontent.com/1815812/119213934-51cbb780-ba99-11eb-875c-be0aa773048f.png)


---
⌨️ com ❤️ por [Ricardo Galeno](https://github.com/ricardogpsf) 😊
