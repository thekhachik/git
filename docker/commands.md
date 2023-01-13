Docker pull  <image’s name> - стянуть образ
Docker build -t <image’s name> - создать образ
Docker run —name <container’s name> <image> - запустить образ, т.е. создать контейнер с именем 

Docker rm <image’s id> - удалить образ
Docker rm <container’s id> - удалить контейнер 
Docker rm $(docker ps -qa) - удалить все контейнеры

Docker images - вывести образы
Docker ps -a - вывести образы, контейнеры и т.д.

Docker start <container’s name> - запустить контейнер
Docker stop <container’s name> - остановить контейнер
Docker pause <container’s name> - поставить на паузу контейнер
Docker unpause <container’s name> - выйти с паузы контейнер

pip install -r requirements.txt
В файле requirements.txt будут содержаться нужны версии инструментов, которые нужно скачать через эту команду для того, чтобы не скачивать в терминале по одному разу каждый язык и т.д.

Если джанго-проекта нет, то docker-compose run django django-admin startproject erik . 
А затем для запуска приложения docker-compose up, для остановки docker-compose down

- Docker image — это неизменяемый образ, из которого разворачивается контейнер. 
- Docker container — развёрнутое и запущенное приложение. 
- Docker registry — репозиторий, в котором хранятся образы. 
- Dockerfile — файл-инструкция для сборки образа.
- Docker compose — инструмент для управления несколькими контейнерами.  Он позволяет создавать контейнеры и задавать их конфигурацию. 

Dockerfile:
1. FROM — задаёт базовый (родительский) образ.
2. LABEL — описывает метаданные. Например — сведения о том, кто создал и поддерживает образ.
3. ENV — устанавливает постоянные переменные среды.
4. RUN — выполняет команду и создаёт слой образа. Используется для установки в контейнер пакетов.
5. COPY — копирует в контейнер файлы и папки.
6. ADD — копирует файлы и папки в контейнер, может распаковывать локальные .tar-файлы.
7. CMD — описывает команду с аргументами, которую нужно выполнить когда контейнер будет запущен. Аргументы могут быть переопределены при запуске контейнера. В файле может присутствовать лишь одна инструкция CMD.
8. WORKDIR — задаёт рабочую директорию для следующей инструкции.
9. ARG — задаёт переменные для передачи Docker во время сборки образа.
10. ENTRYPOINT — предоставляет команду с аргументами для вызова во время выполнения контейнера. Аргументы не переопределяются.
11. EXPOSE — указывает на необходимость открыть порт.
12. VOLUME — создаёт точку монтирования для работы с постоянным хранилищем.

