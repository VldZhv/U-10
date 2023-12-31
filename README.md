## План внедрения автоматизации тестирования
### Перечень автоматизируемых сценариев

**Предусловия: переход к форме записи**

- Переход с главной страницы на страницу формы заявки на курс "Тестировщик" через каталог курсов, раздел "Программирование"
- Переход с главной страницы к странице каталога курсов, раздел "Программирование" через раздел "Направления обучения"
- Переход с футера главной страницы на страницу "Каталог курсов" / "Тестировщик ПО" 
- Переход с футера главной страницы на страницу 
"Популярные курсы" / "Тестировщик ПО" 
- Переход с футера главной страницы на страницу 
"Программирование" / "Тестировщик ПО" 
#### Отправка формы

**Предусловия: требования к содержимому полей при отправке формы**

1. **Поле "Имя":** 
   - Допускаются значения, состоящие минимум из 2х символов на латинице или кириллице, допускается использование дефиса и пробела.

2. **Поле "Телефон":**
   - Либо содержит только цифры (от 9 до 14 цифр).
   - Либо содержит цифры, круглые скобки, пробел, дефис в формате +9 (999) 999-99-99

**Позитивные тестовые сценарии:**

- Ввод имени на кириллице, содержащего 2 и более символа, валидного номера телефона, нажатие на кнопку "Записаться". Успешная отправка формы

- Ввод имени на кириллице, содержащего 2 и более символа, валидного номера телефона, нажатие на кнопку "Получить консультацию". Успешная отправка формы

- Ввод имени на латинице, содержащего 2 и более символа, валидного номера телефона, нажатие на кнопку "Записаться". Успешная отправка формы

- Ввод имени на латинице, содержащего 2 и более символа, валидного номера телефона, нажатие на кнопку "Получить консультацию". Успешная отправка формы



**Негативные тестовые сценарии:**

- Пустая форма "Записаться", нажатие на кнопку "Записаться". Форма не отправляется, поля подсвечиваются красным, сообщение об ошибке

- Ввод в поле "Имя" одного символа на кириллице, валидный номер телефона, нажатие на кнопку "Записаться". Форма не отправляется, поля подсвечиваются красным, сообщение об ошибке

- Ввод в поля "Имя" одного символа на латинице, валидный номер телефона, нажатие на кнопку "Записаться". Форма не отправляется, поля подсвечиваются красным, сообщение об ошибке

- Ввод в поле "Имя" одного символа на кириллице, валидный номер телефона, нажатие на кнопку "Получить консультацию". Форма не отправляется, поля подсвечиваются красным, сообщение об ошибке

- Ввод в поле "Имя" одного символа на латинице, валидный номер телефона, нажатие на кнопку "Получить консультацию". Форма не отправляется, поля подсвечиваются красным, сообщение об ошибке

- Ввод в поле "Имя" валидного значения, в поле "Телефон" невалидного номера, состоящего из менее чем 9 цифр, нажатие на кнопку "Записаться". Форма не отправляется, поля подсвечиваются красным, сообщение об ошибке

- Ввод в поле "Имя" валидного значения, в поле "Телефон"  невалидного номера, состоящего из более чем 14 цифр, нажатие на кнопку "Записаться". Форма не отправляется, поля подсвечиваются красным, сообщение об ошибке

- Ввод в поле "Имя" валидного значения, в поле "Телефон"  невалидного номера, состоящего из более чем 14 цифр, нажатие на кнопку "Получить консультацию". Форма не отправляется, поля подсвечиваются красным, сообщение об ошибке

- Ввод в поле "Имя" валидного значения,в поле "Телефон" навалидного значения, содержащего недопустимые символы, нажатие на кнопку "Получить консультацию". Форма не отправляется, поля подсвечиваются красным, сообщение об ошибке

### Перечень используемых инструментов с обоснованием выбора


- Язык программирования Java, удобен для автоматизации тестирования благодаря своей простоте и логичному синтаксису, использованию принципов ООП, обеспечивающих абстракцию, инкапсуляцию, наследование и полиморфизм, а также гарантирующий безопасность, высокую производительность, надежность и независимость от аппаратной части и ОС

- IntelliJ IDEA, удобна в качестве среды подготовки автотестов

- JUnit5, наиболее современная библиотека для тестирования 

- Selenide, удобен при проведении тестирования веб-интерфейса

- Faker, неоходим для генерации данных при заполнении форм

- Git, система контроля версий

- AppVeyor, распределенный веб-сервис непрерывной интеграции, предназначенный для сборки и тестирования ПО, расположенного на GitHub

- Jira, инструмент для создания баг-репортов

### Перечень необходимых разрешений/данных/доступов
- Разрешение на проведение автоматизированного тестирования
- Разрешение на доступ к требованиям
- Доступ к БД
- Доступ к тестовым данным

### Перечень и описание возможных рисков при автоматизации:
- Зависимость автотестов от текущей реализации веб-элементов, возможная потеря актуальности при даже небольших изменениях UI

- Отсутствие проверки графических аспектов в автотестах, включая оценку адаптивности верстки при различных воздействиях 

### Перечень необходимых специалистов для автоматизации.
Автоматизированный тестировщик (QA Automation Engineer)
### Интервальная оценка с учётом рисков в часах
От 24 до 36 часов