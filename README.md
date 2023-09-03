[![Build status](https://ci.appveyor.com/api/projects/status/r3fct0wy5488xso8?svg=true)](https://ci.appveyor.com/project/PupiYakiSan/automated-testing-coursework)

**Запуск автотестов после клонирования репозитория:**
1. На компьютере должны быть установлены программы IntelliJ IDEA и Docker Desktop
1. Проект открывается в IntelliJ IDEA
1. Запускается Docker Desktop
1. В командной строке IntelliJ IDEA вводится: docker-compose up
1. В новой командной строке IntelliJ IDEA вводится: java -jar artifacts/aqa-shop.jar
1. В новой командной строке IntelliJ IDEA вводится: ./gradlew clean test
1. В той же командной строке вводится: ./gradlew allureserve
