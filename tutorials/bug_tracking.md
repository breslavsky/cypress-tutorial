# Туториал: организуем баг-трекинг в стартапе

Подойдет тем, что хочет научиться доставлять баги разработчикам и организовывать работу по их исправлению.

# 👍 Что сделаем

* Научимся красиво оформлять баг-репорты в **Markdown**.
* Организуем **баг-трекинг** в стартапе.
* Напишем более 10 **баг-репортов** разработчикам.

# 🙋‍️ Перед началом

* У Вас установлен браузер [Google Chrome](https://www.google.com/chrome/)
* У Вас открывается [тестовое приложение](https://qa.epic1h.com)
* У Вас установлено приложение для создания скриншотов и записи экрана или установите [Awesome Screenshot](https://www.awesomescreenshot.com)
* Прочитайте про [Markdown](https://ru.markdown.net.br/nachinaya/)

Создайте текстовый файл `env.txt` на рабочем столе, заполните и сохраните его со своими данными:
* **Устройство:** MacBook M1 Pro (14-inch, 2021) / 32 GB RAM
* **ОС:** macOS Monterey 12.0.1
* **Экран:** Built-in XDR Display 3024x1964
* **Браузер:** Google Chrome 100.0.4896.88 (arm64)
* **Параметры сети:** 90.187.49.33, 100MB, Vodafone Germany

> env - сокращение от environment - окружение

<details>
   <summary>Откуда это взять ❓</summary>

* **Устройство** — посмотрите этикетки на вашем системном блоке или ноутбуке
* **ОС** — посмотрите [видео](https://www.youtube.com/watch?v=VyvSqajg9C4)
* **Экран** — посмотрите короткое [видео](https://www.youtube.com/watch?v=ak53URhvGzI)
* **Браузер** — посмотрите короткое [видео](https://www.youtube.com/watch?v=2l5Ij77DvQk)
* **Параметры сети** — зайдите на сайт https://whatismyipaddress.com/
</details>

# 😍 Живая обратная связь

Каждый вторник и четверг я провожу бесплатные онлайн стендапы в Zoom.

Если у тебя есть вопрос или проблема, подключайся:
- [x] В **20:00** по MSK нажми на [ссылку](https://us05web.zoom.us/j/6630696938)
- [x] Введи пароль `zyx`
- [x] Подними руку или напиши вопрос в чате.
- [x] В случае необходимости, будь готов пошарить свой экран.

@[Anton Breslavsky|https://t.me/breslavsky_anton|https://s.epic1h.com/api/public/dl/nfCyhZhd?inline=true]

Что бы следить за анонсами новых туториалов подписывайся на [телеграмм канал](https://t.me/epic_one_hour)

***

# 🔢 Шаги

Вас взяли **QA стажером** в стартап в котором разрабатывают инновационный платежный сервис **iBank**.

На текущий момент тестирование проводилось разработчиками самостоятельно.

**Ваша цель:** организовать процессы тестирования **Веб-приложения iBank**

## 1. Баг-лист

- [x] Открой **Markdown** редактор https://markdownlivepreview.com/
- [x] Скопируй в левую часть редактора исходное содержимое.

```markdown
# Баг-лист приложения iBank
* [ ] 🐞 [Орфографическая ошибка в слове](https://tinyurl.com/yxkduuxy)
* [ ] 🐞 [Поле ввода пароль не скрывает введенные символы](https://tinyurl.com/3zy9ywb3)

```

- [x] Открой ссылки на баги, и проанализируй скриншоты.

**Баг-лист** — это список ошибок со ссылками на снимки или записи экрана.

> **Инсайт**
> 
> Любая работа по поиску багов начинается с составления баг-листа!

**Markdown** — язык разметки текста — **must have** для ИТ индустрии!

> **Инсайт**
>
> В IT сфере любой документ должен быть качественно и красиво оформлен.
> Эмпатия при этом является основой. 
>
> После написания любого документа Антону (или для кого ты пишешь) задай вопросы: 
> * насколько Антону удобно будет читать мой документ?
> * насколько Антону будет понятно, что я написал?
> * в документе нет орфографических ошибок?
> * оформление документа содержит заголовки, списки, ссылки, картинки, скриншоты?

В Markdown пишется документация, оформляются **Wiki** базы знаний, файлы **README**, описание задач и т.д.

**Markdown** содержит специальный синтаксис для оформления:
* заголовков,
* параграфов,
* списков,
* ссылок,
* примеров кода,
* вставки картинок
* и т.д.

- [x] Открой в **Chrome** веб-приложение **iBank** https://qa.epic1h.com/
- [x] Найди все ошибки из баг-листа.

***

**Как можно сообщить разработчикам о данных ошибках?**
* Подойти и сказать словами.
* Написать сообщение в чате.
* Позвонить по телефону.
* Оставить записку на столе.
* Попросить маму передать информацию.

<details>
  <summary>Да или нет?</summary>

**Нет! Нет! Пожалуйста, нет!**

<iframe src="https://giphy.com/embed/8vUEXZA2me7vnuUvrs" 
   width="480" height="480" frameBorder="0" class="giphy-embed"></iframe>

**В баг-репорте — да!️**

 <iframe src="https://giphy.com/embed/Od0QRnzwRBYmDU3eEO" 
   width="480" height="480" frameBorder="0" class="giphy-embed"></iframe>  
</details>

## 2. Узнаем про баг-репорт

> Официальное определение баг-репорта.

**Баг-репорт** — отчет о несоответствии фактической работы (функционирования) программы и запланированных требований описанных в техническом задании на программу.

Требования к программе это:
* Какие функции выполняет программа.
* Как выглядит и работает ее интерфейс.
* Насколько программа безопасна и надежна.
* И т.д.

> **Инсайт**
>
> Техническое задание не всегда бывает и не всегда может содержать все требования в деталях.

**Поэтому, от себя, я бы еще добавил:** а так же отчет, о несоответствии работы программы общепринятым отраслевым практикам.

> **Пример**
> 
> В техническом задании например, может быть не написано, что все поля ввода пароля должны скрывать введенный текст звездочками, что бы не компрометировать пользователя.
> Но это не значит, что разработчик не должен этого сделать. Что такое компрометация? Представьте, что вы набираете пин-код, он отражается на экране банкомата, а сзади стоит подозрительный тип 🤨

**Баг** — это дефект, ошибка, проблема описанная в **бег-репорте** которая должна быть исправлена.

Что бы исправить ошибку хороший **баг-репорт** должен позволить:
* Понять суть проблемы и ее важность.
* Воспроизвести проблему.

***

<details>
  <summary>Аттрибуты баг-репорта уровня like a boss 😎</summary>

<iframe src="https://giphy.com/embed/ZTwVNm5aH7oOc" 
   width="480" height="303" frameBorder="0" class="giphy-embed"></iframe>
</details>

* Одна ошибка — один репорт — **атомарность**
* Шаги для обнаружения бага сможет повторить ваша бабушка — **воспроизводимость**
* Лучше написать больше, чем потом утонуть в уточнениях (время) с разработчиком — **полнота**
* Не писать лишнего — **лаконичность**
* Профессиональное оформление и лучшие практики — **красота**
* Разработчик должен «кайфануть» от бага — **эмпатия**

***

## 3. Твой первый баг-репорт

- [x] В новой вкладке снова открой **Markdown** редактор https://markdownlivepreview.com/ 
- [x] Скопируйте в него исходное содержимое [примера баг-репорта](https://raw.githubusercontent.com/breslavsky/hello-cypress/main/artefacts/bug_report.md)

***

- [x] Проанализируй содержание и разделы баг репорта.
- [x] Актуализируй баг-репорт:
  * исправь дату обнаружения,
  * вставь параметры своего окружения.

> Помнишь при подготовке ты делал файл `env.txt`?

***

- [x] Удали в разметке **баг-репорта** теги `<details> ... </details>` и их содержимое в редакторе.

***

## 4. Организация **Баг-трекера**

### 4.1 Настройка **Канбан-доски**

- [x] Открой **таск-трекер** [Trello](https://trello.com) и создай новую канбан-доску **iBank**
- [x] Создай списки: **Баг найден**, **Баг исправляется**, **Баг исправлен**, **Баг отклонен**, **Баг исправлен и проверен**

***

### 4.2 Карточка бага и разработчик

- [x] Создай новую карточку **Орфографическая ошибка в слове** и скопируй содержимое **баг-репорта** в описание карточки.
- [x] Добавь лейбл зеленого цвета для приоритета **низкий**

***

- [x] Пригласи разработчика **ivan.ivanov@gmail.com** на свою доску и назначь ему данный билет.
- [x] Перемести карточку в состояние **Баг исправлен**.

***

### 4.3 Проверка исправления

- [x] Найдите в комментарии к билету ссылку на исправленную версию приложения.

<details>
   <summary>Комментарий разработчика</summary>

Спасибо за отличный баг 🙏🏻 Я все поправил!️

Держи ссылку на релиз с исправлением https://qa.epic1h.com/?v=1.1

</details>

***

- [x] Переместите билет в состояние **Баг исправлен и проверен**

Не забудьте сказать разработчику в комментариях спасибо ❤️

❓ В каком случае билет может быть перемещен в список **Баг отклонен**?

<details>
   <summary>Ответ</summary>

Когда разработчик:
* не смог воспроизвести баг,
* когда это не баг, а нормальное поведение программы,
* когда баг уже был исправлен ранее.

Он напишет тебе причину в комментариях к билету.
</details>

***

## 5. Баг-репорт на поле ввода пароля

- [x] Составь баг-репорт в редакторе для бага 🐞 [Поле ввода пароль не скрывает введенные символы](https://www.awesomescreenshot.com/video/9015550?key=6d7d2d74c1c3481ea13797fed3845ee2)
- [x] Создайте новую карточку в Trello для бага.

***

<details>
   <summary>Баг-репорт на поле ввода пароля</summary>

* **Номер**: 2
* **Наименование**: Поле ввода пароль не скрывает введенные символы
* **Тип:** Ошибка безопасности
* **Серьезность:** 🟢 незначительная
* **Приоритет:** 🔴 высокий

**Шаги для воспроизведения**

1. Открыть главную страницу iBank `/`
1. Ввести в поле пароль: 123456

**Фактический результат**

Пользователь видит введенный им пароль.

**Ожидаемый результат**

Пользователь видит вместо символов пароля `*`

**Мотивация**

**Лучшая практика:** интерфейс программы не должен компрометировать пользователя.

</details>

# 🤩 Что дальше?

- [x] Создай в **Трелло** отдельную задачу: **Тестирование приложения iBank**
- [x] В качестве описания добавь баг-лист.

## Баг-лист для приложения iBank
1. 🐞 Ошибка в заголовке вход в систему

<details>
   <summary>Где?</summary>

В заголовках не ставятся точки в конце, правильно — **Вход в систему**
</details>

2. 🐞 Ошибка в сообщении введите логин или пароль

<details>
   <summary>Где?</summary>

Правильно — **Введите логин и пароль**
</details>

3. 🐞 Заголовок вход в систему обрезан снизу
4. 🐞 Поле пароль смещено наверх
5. 🐞 Размер шрифта полей логин и пароль разный
6. 🐞 Ширина поля логин не вмещает вспомогательный текст
7. 🐞 Несовместимые цвета в приветствии
8. 🐞 После неудачного входа поле логин сбрасывается
9. 🐞 Ошибка локализации сообщения при входе
10. 🐞 Сообщение об ошибке показывается 2 раза
11. 🐞 Не отражается прогресс входа
12. 🐞 Кнопка войти нажимается несколько раз подряд
13. 🐞 Поле пароль не отображается в Opera
14. 🐞 На смартфоне форма входа обрезается

## Чек-лист по задачам
- [x] Самостоятельно найди все ошибки из баг-листа.
- [x] Добавь скриншоты или записи экрана в виде ссылок в Markdown для данного баг-листа.
- [x] Обозначь и обведи баги на скриншотах.
- [x] Для каждой ошибки создай отдельную карточку и оформи баг-репорт.
- [x] Расставь приоритеты, и отсортируй карточки.
- [x] Сделай свою доску публичной и доступной по ссылке.
- [x] Отправите ссылку в канал **qa_feedback** с просьбой коллег из [сообщества](https://t.me/epic_one_hour_community) провести оценку своих баг-репортов.
- [x] Попробуйте найти еще баги.

<details>
  <summary>Что делать?</summary>
  <p></p>

|  Логин  | Пароль |
|:-------:|--------|
|   bob   | qwerty |
| chester | 123456 |
| marry   | qwerty |

* Войди от разных пользователей.
* Переведи от **chester** к **bob** 100 рублей.
* Выйди из **chester**, зайди под **bob** и проверьте баланс.
* Попробуй перевести 0 рублей.
* Попробуй перевести -100 рублей.
* Попробуй переводить деньги от разных пользователей.

</details>

> Уважаемые коллеги, прошу Вас провести ревью и дать обратную связь по составлению баг-репортов.
>
> Ссылка на баг-трекер https://trello.com/...
> 
> Заранее благодарю 🙏🏻

После комментариев от коллег:
- [x] Войди на обновленную версию https://qa.epic1h.com/?v=1.2
- [x] Проверь каждый баг на исправление.
- [x] Исправленные баги перемести в состояние **Исправлен и проверен**.

# Фидбек пожалуйста 🙏

? Полезный материал ?
* 🤩 Очень полезный материал
* 😃 В целом полезный
* 😐 Возможно что-то пригодится
* 😒 Нет ничего полезного
* 😬 Абсолютно бесполезно

? Все ли было понятно ?
* 🤩 Все понятно на 100%
* 😃 В целом все понятно
* 😐 Что-то понятно, что-то нет
* 😒 Понял только малую часть
* 😬 Ничего не понял

? Как тебе такой формат туториала ?
* 🤩 Очень удобно
* 😃 Мне понравилось
* 😐 Нормально
* 😒 Не удобно
* 😬 Ужасно

# Артефакты
1. [Пример баг-репорта](artefacts/bug_report.md)
2. [Идеальный баг-репорт](artefacts/perfect_bug_report.md)

# Читать и смотреть
1. [Доступно написано про баг и баг репорт](https://beqa.pro/blog/баг-и-баг-репорт)
2. [Правила написания предварительных шагов в тест-кейсах](https://habr.com/ru/post/481628/)

# Вопросы на собеседованиях
* Что такое жизненный цикл бага?
* Что делать, если разработчик утверждает, что найденный дефект таковым не является?
* Когда баг попадает в статус **Отложен / Deferred**?
* Как вы понимаете, что перед Вами качественный продукт?
* Какие атрибуты баг-репорта? Какие основные поля для заполнения?
* Приведите примеры серьезного, но не приоритетного бага?
