# back
# устанавливаем самую лёгкую версию JVM
FROM openjdk:8-jdk-alpine

# указываем ярлык. Например, разработчика образа и проч. Необязательный пункт.
LABEL maintainer="2262288@gmail.com"

# указываем точку монтирования для внешних данных внутри контейнера (как мы помним, это Линукс)
VOLUME /tmp

# внешний порт, по которому наше приложение будет доступно извне
EXPOSE 8099

# указываем, где в нашем приложении лежит джарник
ARG JAR_FILE=build/libs/rebounder-chain-backend-0.0.2.jar

# добавляем джарник в образ под именем rebounder-chain-backend.jar
ADD ${JAR_FILE} rebounder-chain-backend.jar

# команда запуска джарника
ENTRYPOINT ["java","-jar","/rebounder-chain-backend.jar"]