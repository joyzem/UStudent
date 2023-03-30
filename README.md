# UStudent

Для студентов существует множество приложений, упрощающих выполнение ежедневных задач, помогающих в поиске и обработке информации и даже являющимися полноценными журналами, куда можно записывать расписание, домашние задания, события и т.д. Несмотря на богатый функционал, «добраться» до него очень трудно. Главная проблема этих приложений заключается в их универсальности. Или же, иначе говоря, в ручном заполнении всего того объема информации о расписании, дисциплинах, преподавателях и т.д. К тому же на рынке полностью отсутствуют приложения для старост учебных групп. В связи с этим было принято решение разработать собственное мобильное приложение для студентов — **«UStudent»**. 

Приложение является частью создаваемой платформы «UStudent».

В данном репозитории представлена основная информация о приложении. В конце страницы находится раздел с научными статьями о платформе и приложении, а также информация об авторах.

## Функционал

Вся функциональность работает в рамках университета «ФГБОУ ВО Кубанский государственный аграрный университет имени И.Т. Трубилина»
- Авторизация пользователей через номер группы;
- Просмотр расписания по группам, преподавателям и аудиториям;
- Составление списков присутствующих или отсутствующих студентов на занятиях;
- Возможность сменить группу на экране настроек.

## Планируемый функционал

- Авторизация пользователей через личный кабинет студента с помощью пароля и логина
- Домашние задания (индивидуальных и общедоступных)
- События. ToDo с возможность старосты создавать события для группы, которые необходимо выполнить (выбор темы курсовой, подготовка докладов, сбор средств)
- Студенческие мудрости. Раздел, в котором студенты могут проявить своё остроумие и поднять настроение и боевой дух другим студентам, опубликовав свою мудрость.

## Дизайн

Дизайн приложения соответствует гайдлайнам [Material Design 2](https://m2.material.io/design/guidelines-overview)

### Экран расписания

![Экран расписания](/assets/schedule.png "Расписание")

### Экран посещаемости

![Экран посещаемости](/assets/attendance.png "Посещаемость")

### Экраны доработки
![Экран доработки](/assets/in-works.png "Доработка")
### Боковое меню

![Боковое меню](/assets/sidenav.png "Меню")

### Экран входа
![Экран входа](/assets/login.png "Вход")
### О проекте
![Экран проекта](/assets/about-project.png "Проект")
## Релиз

Приложение было выпущено в [RuStore](https://apps.rustore.ru/app/ru.ustudentplatform.ustudent), а также в [Telegram-канале](https://t.me/ustudentapp) проекта.
С помощью инструментов AppMetrica была собрана и проанализирована статистика по использованию приложения за первые 2-3 недели.
Данные по статистике приведены в таблице:
Показатель | Значение
-- | --
Количество уникальных пользователей | 286
Удержание пользователя после установки | В среднем: 53,975%
1 день | 55.6 %
2 день | 51.3%
3 день | 53%
4 день | 56%
Отсутствие критических ошибок | 98,71% (затем 100% после обновления)
Среднее количество сессий за день | 4

## Архитектура

Приложение разделено на слои и модули. Вдохновением для разбиения на модули стала большая сложность поддержки текущего кода и добавления новых фич. В качестве образца послужил проект [Now in Android](https://github.com/android/nowinandroid) с его графом модулей:

![Граф модулей](/assets/modularization-graph.drawio.png)

Используются: Clean Architecture, MVVM, принципы SOLID, UDF, KISS, DRY

## Технологии

ЯП | Kotlin
-- | --
DI | Hilt
UI | Jetpack Compose
Async | Kotlin Coroutines
Reactive Programming | Flow + State
Network | Retrofit + Moshi
Data persistence | Room + Proto DataStore
Build-logic | .toml + .kts + Build conventions
Etc. | FCM, App Metrica, KSP, secrets

## Научные статьи и тезисы

- [Единая студенческая платформа](articles/единая_студенческая_платформа.docx)
- [Мобильное приложение "UStudent"](articles/мобильное_приложение_ustudent.docx)
- [Публикация мобильного приложения для студентов "UStudent"](/articles/публикация.docx)
- [Презентация для конкурса IQ-года](iq/презентация.pdf)
- [Описание платформы для конкурса IQ-года](iq/платформа.docx)

## Авторы
- Газизов Родион. Автор проекта, Android-разработчик, дизайнер, product-project-manager, технический писатель;
- \[Имя скрыто по просьбе разработчика\]. Backend-разработчик;
- Черногаев Матвей. Тестировщик.