FROM openjdk:11-jre-slim

# Устанавливаем необходимые пакеты
RUN apt-get update && apt-get install -y \
    x11-apps \
    xauth \
    libxtst6 \
    && rm -rf /var/lib/apt/lists/*


ENV DISPLAY=:0

WORKDIR /apps
# Копируем файл calc.jar внутрь контейнера
COPY calc.jar apps/

# Запускаем приложение при старте контейнера
CMD ["java", "-jar", "/PR5/calc/calc.jar"]
