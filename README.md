# [![Send](./assets/icon.svg)](https://github.com/alexeylesin/send/) LesinSend

Форк ранее закрытого сервиса [Firefox Send](https://github.com/mozilla/send/). Mozilla перестали его поддерживать,
поэтому я решил поставить его к себе на хостинг и сделать публичным. Данный репозиторий основан
на [другом форке](https://github.com/timvisee/send).

- Удалены все упоминания _Mozilla_ и _Firefox_
- Оставлена совместимость с [`ffsend`][ffsend] (CLI)
- Были активированы некоторые экспериментальные функции

Гайд по установке на Docker можно найти здесь: [docs/docker.md](docs/docker.md)

---

**Документация:** [FAQ](docs/faq.md), [Шифрование](docs/encryption.md), [Сборка](docs/build.md), [Docker](docs/docker.md), [Метрика](docs/metrics.md), [Больше](docs/)

---

## Содержание

* [Информация](#информация)
* [Зависимости](#зависимости)
* [Разработка](#разработка)
* [Команды](#команды)
* [Конфигурация](#конфигурация)
* [Локализация](#локализация)
* [Развертывание](#развертывание)
* [Клиенты](#клиенты)
* [Лицензия](#лицензия)

---

## Информация

Экспериментальный сервис, позволяющий отправлять зашифрованные файлы другим людям.

---

## Зависимости

- [Node.js 12.x](https://nodejs.org/)
- [Redis server](https://redis.io/) (опционально для разработки)
- [AWS S3](https://aws.amazon.com/s3/) или совместимый сервис (опционально)

---

## Разработка

Для запуска тестового сервера, воспользуйтесь данными командами:

```sh
npm install
npm start
```

Затем, перейдите на http://localhost:8080

---

## Команды

| Команда          | Описание    |
|------------------|-------------|
| `npm run format` | Форматирует фронтенд и серверный код, используя **prettier**.
| `npm run lint`   | Оптимизирует CSS и JavaScript код.
| `npm test`       | Запускает несколько **mocha** тестов.
| `npm start`      | Запускает сервер в конфигурации для разработки.
| `npm run build`  | Собирает ассеты для продакшена.
| `npm run prod`   | Запускает сервер в конфигурации для продакшена.

---

## Конфигурация

Сервер конфигурирован с переменными средами. Смотрите [server/config.js](server/config.js) для всех настроек и [docs/docker.md](docs/docker.md) для примеров.

---

## Локализация

Гайд по настройке локализации - [docs/localization.md](docs/localization.md)

---

## Развертывание

Гайд по развертыванию - [docs/deployment.md](docs/deployment.md)

---

## Клиенты

- Веб-часть: _этот репозиторий_
- Терминал: [`ffsend`](https://github.com/timvisee/ffsend)
- Android: _смотрите раздел [Android](#android)_

#### Android

Реализация под Android находится в директории `android`,
и может быть просмотрена локально для удобства тестирования и редактирования, запустив `ANDROID=1 npm
start` и затем открыв <http://localhost:8080>. CSS и файлы изображений
находятся в папке `android/app/src/main/assets`.

---

## Лицензия

[Mozilla Public License Version 2.0](LICENSE)

[qrcode.js](https://github.com/kazuhikoarase/qrcode-generator) имеет лицензию MIT

---
