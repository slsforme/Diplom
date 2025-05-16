# https://prirodarazumadev.ru/

# Для проверки работоспособности работы с Яндекс.Диск необходимо внести СВОЙ токен в .env
Как это сделать? - https://yandex.cloud/ru/docs/iam/operations/authentication/manage-api-keys

Базовые данные для входа за админа:
login: **admin123**
password: **admin123**

Базовые данные для входа за админа:
login: **login123**
password: **login123**

## Как развернуть сайт локально?

1. Необходимо клонировать репозиторий:
``
2. Далее надо перейти в клонированный репозиторий:
``
3. Далее надо подтянуть сабмодули:
``
4. Также необходимо сменить URL на frontend, для этого надо перейти в следующие файлы:
  - `web/frontend/priroda-razuma/src/features/services/api.ts`
  - `web/frontend/priroda-razuma/src/features/services/api.ts`
В данных файлах надо поменять baseURL на задокументированный URL - **http://localhost/api/v1**
5. Перед развёртыванием из корня проекта надо перейти в корень проекта для сайта:
``
6. Теперь для развёртывания необходимо прописать 
`docker-compose -f local-docker-compose.yml up`
7. Для проверки работы сайта надо перейти на URL **http://localhost**
8. Для проверки работы API необходимо открыть документацию по ссылке **http://localhost/api/v1/docs**


