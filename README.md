# Restful Booker API tests

**Публичная документация Postman:** https://documenter.getpostman.com/view/59042488/2sBYHSxg8z

Postman-коллекция для тестового REST API [Restful Booker](https://restful-booker.herokuapp.com/). Коллекция содержит 12 последовательных запросов и 26 автоматических проверок ответа.

## Запуск

### Postman

1. Импортируйте `restful-booker.postman_collection.json` через **Import → Files**.
2. Запустите коллекцию через **Run** в исходном порядке.
3. Если тестовый стенд сменил демонстрационные учетные данные, поменяйте `username` и `password` в переменных коллекции.

Коллекция сама получает токен, генерирует данные, сохраняет ID созданной брони, передает их в следующие запросы и удаляет запись в конце. Окружение Postman не требуется.

### Newman

Нужны Node.js и pnpm. В корне проекта выполните:

```bash
pnpm install --frozen-lockfile
pnpm test:api
```

Или без установки проекта:

```bash
