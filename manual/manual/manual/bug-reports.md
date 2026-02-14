# Bug Reports — SauceDemo (samples)

> Примечание: записи ниже оформлены как примеры структуры баг-репорта для портфолио (training samples).

---

**BUG-LOGIN-001 — Error message не очищается после успешного логина**
- Environment: Windows 10, Chrome (latest)
- Preconditions: ранее выполнена попытка логина с неверным паролем (появилось сообщение об ошибке)
- Steps to reproduce:
  1) Ввести username: `standard_user`
  2) Ввести password: `secret_sauce`
  3) Нажать `Login`
- Actual result: пользователь попадает на страницу Products, но сообщение об ошибке остаётся отображаться (или “залипает”)
- Expected result: после успешного логина сообщение об ошибке не должно отображаться
- Severity: Minor
- Priority: Low
- Attachment: (скрин/видео при наличии)

---

**BUG-CART-001 — Badge корзины не обновляется после удаления товара**
- Environment: Windows 10, Chrome (latest)
- Preconditions: пользователь авторизован
- Steps to reproduce:
  1) На Products добавить 2 товара
  2) Перейти в корзину
  3) Удалить 1 товар
- Actual result: в корзине товар удалён, но badge корзины продолжает показывать `2`
- Expected result: badge должен обновиться и показывать `1`
- Severity: Major
- Priority: Medium
- Attachment: (скрин/видео при наличии)

---

**BUG-PROD-001 — Сортировка “Price (low to high)” сортирует некорректно**
- Environment: Windows 10, Chrome (latest)
- Preconditions: пользователь авторизован, открыта страница Products
- Steps to reproduce:
  1) В сортировке выбрать `Price (low to high)`
  2) Сравнить цены первого и второго товара в списке
- Actual result: порядок товаров не соответствует возрастанию цены
- Expected result: товары должны быть отсортированы по цене по возрастанию
- Severity: Major
- Priority: Medium
- Attachment: (скрин/видео при наличии)

---

**BUG-NAV-001 — После Logout можно вернуться на страницу Products кнопкой “Back”**
- Environment: Windows 10, Chrome (latest)
- Preconditions: пользователь авторизован
- Steps to reproduce:
  1) Открыть меню
  2) Нажать `Logout`
  3) Нажать кнопку браузера “Back”
- Actual result: открывается страница Products с данными (или частично доступный контент)
- Expected result: после Logout доступ к Products должен требовать повторный логин
- Severity: Critical (если реально даёт доступ) / Major (если показывает, но не даёт действовать)
- Priority: High
- Attachment: (скрин/видео при наличии)
