# https://prirodarazumadev.ru/

Для правильной работы обоих приложений рекомендуется копировать с Github.

Как это сделать?
1. Установить git - https://git-scm.com/book/en/v2/Getting-Started-Installing-Git
2. Скопируйте репозиторий при помощи команды `git clone https://github.com/slsforme/Diplom.git`
3. Подтяните сабмодули: `git submodule update --init --remote --recursive`

**Для проверки работоспособности работы с Яндекс.Диск необходимо внести СВОЙ токен в .env**
Как создать свой токен? - https://yandex.cloud/ru/docs/iam/operations/authentication/manage-api-keys

Базовые данные для входа за админа:
login: **admin123**
password: **admin123**

Базовые данные для входа за педагога:
login: **login123**
password: **login123**

## Как развернуть сайт локально?

Перед развёртыванием сайта необходимо скачать Docker и все необходимые плагины, включая docker compose
Описание установки Docker расписано в Приложении Д.
Также рекуомендуется просмотреть данные ресурсы:
- https://docs.docker.com/compose/install/
- https://docs.docker.com/compose/install/linux/

1. Необходимо клонировать репозиторий:
`git clone https://github.com/slsforme/Diplom.git`
2. Далее надо перейти в клонированный репозиторий:
`cd Diplom`
3. Далее надо подтянуть сабмодули:
`git submodule update --init --remote --recursive`
4. Также необходимо сменить URL на frontend, для этого надо перейти в следующие файлы:
  - `web/frontend/priroda-razuma/src/features/services/api.ts`
  - `web/frontend/priroda-razuma/src/features/services/api.ts`
В данных файлах надо поменять baseURL на задокументированный URL - **http://localhost/api/v1**
5. Перед развёртыванием из корня проекта надо перейти в корень проекта для сайта:
`cd web`
6. Теперь для развёртывания необходимо прописать 
`docker compose -f local-docker-compose.yml up`
7. Для проверки работы сайта надо перейти на URL **http://localhost**
8. Для проверки работы API необходимо открыть документацию по ссылке **http://localhost/api/v1/docs**


