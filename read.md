
# 📖 **Руководство по использованию User-Bot**

## 🔍 **Основные команды**  
- **`help`** — Показывает список доступных команд и их описание.  
- **`time`** — Показывает текущее время в выбранных городах мира.  
- **`info <user_id | username>`** — Предоставляет информацию о пользователе, включая ID, имя, username и другое.  
- **`weather <город>`** — Показывает подробную информацию о погоде в указанном городе, включая текущую погоду, ветер, влажность и прогнозы.  

### **Пример вывода команды `weather`:**  
```
🌡 ПОГОДА НА СЕГОДНЯ (Город)
⛅️ Текущая погода: Ясно, +25°C
↖️ Ветер: 5 м/с, влажность: 60%
🌤 Прогноз на сегодня: +25°C до +30°C
☀️ Прогноз на завтра: +20°C до +28°C
☁️ Прогноз на послезавтра: +18°C до +24°C
```

- **`spamattack <количество>`** — Начинает спам стикерами в указанном чате. _(Список стикеров настраивается через `STICKER_ID`.)_  
- **`stopspam`** — Останавливает активный спам.  

> ❗ **Используйте функции спама осторожно. Чрезмерное использование может привести к блокировке вашего аккаунта!**

---

## 🎵 **Музыкальные команды**  
- **`music <название>`** — Выполняет поиск музыки по названию и выводит список результатов.  
- **`download <номер>`** — Загружает трек из результатов поиска по указанному номеру.  
- **`clear_downloads`** — Удаляет все загруженные песни из локального хранилища.  

> ⚙️ **Необходимое программное обеспечение:**  
Для загрузки музыки требуется FFmpeg.  
Установите его перед использованием этой функции:  
- **MacOS:** `brew install ffmpeg`  
- **Ubuntu:** `sudo apt-get install ffmpeg`  
- **Windows:** Скачайте с [ffmpeg.org](https://ffmpeg.org).  

❗ **Обратите внимание, что процесс загрузки может занять некоторое время в зависимости от скорости интернета.**

---

## 🤖 **AI команды**  
- **`set_model <model_name>`** — Устанавливает модель AI для использования:  
  - `g4f` — GPT-4 Turbo без необходимости в API-ключе.  
  - `gemini` — Генеративный AI от Google, поддерживает сложные запросы.  
  - `chatgpt` — Надёжная модель OpenAI GPT-4.  
- **`gpt <текст>`** — Отправляет запрос к установленной модели AI и возвращает ответ.  
- **`clear_context`** — Очищает историю общения с AI, что полезно для новых запросов.  

---

## 🎮 **Развлечения**  
- **`meme`** — Отправляет случайный мем из популярных источников.  
- **`duel @username`** — Вызывает другого пользователя на дуэль.  

### **Механика дуэли:**  
1. Отправьте команду `/duel @username`, чтобы предложить дуэль.  
2. Пользователь должен принять или отклонить вызов в течение 60 секунд.  
3. Победитель выбирается случайно.  

После дуэли бот обновляет статистику побед и поражений для каждого участника.  

---

## ⚙️ **Настройки**  
- **`set_prefix <символ>`** — Изменяет стандартный префикс для команд.  
  _(По умолчанию используется `/`.)_  

---

## 💡 **Примеры использования команд**  
- **`weather Москва`** — Узнать погоду в Москве.  
- **`info @username`** — Получить информацию о пользователе с username.  
- **`music In The End Linkin Park`** — Найти песню "In The End" от группы Linkin Park.  
- **`set_prefix !`** — Установить новый префикс для команд (! вместо /).  

---

## 🪄 **Особенности AI**  
**Поддерживаемые AI модели:**  
1. **Gemini** — ИИ от Google, оптимизирован для сложных задач.  
2. **G4F** — Бесплатный доступ к GPT-4 Turbo, не требует API.  
3. **ChatGPT** — Модель от OpenAI, надёжная и точная.  

**Выбор модели AI:**  
Используйте `/set_model <model_name>`, чтобы переключаться между моделями. Например:  
```
/set_model chatgpt
```

---

## 🚨 **Важно знать**  
1. **Риски при использовании спама:**  
   Спам-функции могут привести к блокировке вашего Telegram-аккаунта, особенно в публичных чатах.  

2. **Ограничения API Gemini:**  
   API от Google может отклонить запросы с неподобающим содержанием (например, NSFW).  
   Пример ошибки:  
   ```
   HARM_CATEGORY_SEXUALLY_EXPLICIT probability: HIGH
   ```

3. **Смена аккаунта в боте:**  
   Если вы хотите использовать другой Telegram-аккаунт:  
   - Удалите файл `mybot.session` в папке с ботом.  
   - Перезапустите бота и войдите с нового аккаунта.  

---

## 🛠 **Начало работы**  
1. **Установка зависимостей:**  
   Убедитесь, что все библиотеки установлены:  
   ```
   pip install -r requirements.txt
   ```  
2. **Первый запуск:**  
   При первом запуске бот запросит ваш номер телефона и код подтверждения для входа.  
3. **Настройка:**  
   По желанию, настройте модель AI и префикс команд.  

---

## 💬 **Поддержите проект**  
Если вам понравился проект, поставьте звезду ⭐ на [GitHub](https://github.com/mikayilaz/TGUser-Bot) и поделитесь с друзьями. Ваши отзывы и предложения помогут сделать бота лучше!  

> **Автор:** [mikayilaz](https://github.com/mikayilaz).  

✨ **Сделайте вклад в проект и помогите создать лучший инструмент для автоматизации Telegram!**  