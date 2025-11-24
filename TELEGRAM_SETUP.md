# 📱 Настройка уведомлений в Telegram

## Шаг 1: Создание Telegram бота

1. Откройте Telegram и найдите бота **@BotFather**
2. Отправьте команду `/newbot`
3. Придумайте имя для бота (например: `StudHelp Notifications Bot`)
4. Придумайте username для бота (должен заканчиваться на `bot`, например: `studhelp_notifications_bot`)
5. **Скопируйте токен**, который даст вам BotFather (выглядит как: `123456789:ABCdefGHIjklMNOpqrsTUVwxyz`)

## Шаг 2: Получение вашего Chat ID

Есть несколько способов:

### Способ 1: Через специального бота
1. Найдите бота **@userinfobot** или **@getidsbot** в Telegram
2. Начните с ним диалог (отправьте `/start`)
3. Бот покажет ваш `id` - это и есть ваш Chat ID (число, например: `123456789`)

### Способ 2: Через вашего бота
1. Напишите вашему боту любое сообщение
2. Откройте в браузере: `https://api.telegram.org/botВАШ_ТОКЕН/getUpdates`
   (замените `ВАШ_ТОКЕН` на токен из шага 1)
3. Найдите в ответе `"chat":{"id":123456789}` - это ваш Chat ID

## Шаг 3: Настройка на сайте

1. Откройте файл `index.html`
2. Найдите строки (около строки 920):
   ```javascript
   const TELEGRAM_BOT_TOKEN = 'YOUR_BOT_TOKEN_HERE';
   const TELEGRAM_CHAT_ID = 'YOUR_CHAT_ID_HERE';
   ```
3. Замените `YOUR_BOT_TOKEN_HERE` на токен из шага 1
4. Замените `YOUR_CHAT_ID_HERE` на Chat ID из шага 2

Пример:
```javascript
const TELEGRAM_BOT_TOKEN = '123456789:ABCdefGHIjklMNOpqrsTUVwxyz';
const TELEGRAM_CHAT_ID = '123456789';
```

## Шаг 4: Проверка

1. Сохраните файл `index.html`
2. Закоммитьте и запушьте изменения:
   ```bash
   git add index.html
   git commit -m "Настроен Telegram бот"
   git push origin main
   ```
3. Откройте сайт и отправьте тестовую заявку
4. Проверьте, пришло ли сообщение в Telegram

## ⚠️ Важно

- **Не публикуйте токен бота** в публичных репозиториях
- Если токен скомпрометирован, создайте нового бота через @BotFather
- Chat ID - это ваш личный идентификатор, его можно не скрывать

## 🎉 Готово!

Теперь все заявки с сайта будут приходить вам в Telegram!

