# Задание 2: Проектирование API

## **REST API Запрос**

При открытии экрана «Выберите магазин» мобильное приложение делает `GET` запрос к бэкенду. Для соблюдения паттерна Backend-For-Frontend (BFF), запрос не требует сложных параметров, так как вся агрегация происходит на сервере.

- **Метод:** `GET`
- **Endpoint:** `/api/v1/partners/stores`
- **Headers:**
  - `Authorization: Bearer <token>` (если требуется авторизация)
  - `Accept-Language: ru-RU`
  - `Client-Timezone: Europe/Moscow` (опционально, для расчета времени доставки)

---

## **Пример ответа (JSON)**

```json
{
  "status": "success",
  "data": {
    "stores": [
      {
        "id": "101",
        "name": "METRO",
        "delivery_info": "Ближайшая доставка сегодня 21:00-23:00",
        "logo_url": "https://static.petrushka.ru/partners/metro-logo.png",
        "redirect_url": "https://metro.ru/partner-link/petrushka",
        "is_fast_delivery": false
      },
      {
        "id": "102",
        "name": "Ашан",
        "delivery_info": "Ближайшая доставка сегодня 18:00-20:00",
        "logo_url": "https://static.petrushka.ru/partners/auchan-logo.png",
        "redirect_url": "https://auchan.ru/partner/campaign",
        "is_fast_delivery": false
      },
      {
        "id": "103",
        "name": "ВкусВилл",
        "delivery_info": "Быстрая доставка от 20 до 60 минут",
        "logo_url": "https://static.petrushka.ru/partners/vkusvill-logo.png",
        "redirect_url": "https://vkusvill.ru/express",
        "is_fast_delivery": true
      },
      {
        "id": "104",
        "name": "ВИКТОРИЯ",
        "delivery_info": "Ближайшая доставка сегодня 17:00-19:00",
        "logo_url": "https://static.petrushka.ru/partners/victoria-logo.png",
        "redirect_url": "https://victoria-group.ru/order",
        "is_fast_delivery": false
      }
    ]
  }
}
