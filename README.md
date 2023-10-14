# Лабораторная работа 3

## Вариант `18881`

<img alt="anime" src="./.resources/anime.gif" height="200">

> Jakarta Server Facepalm

|.pdf|.docx|
|-|-|
| [report](./docs/report.pdf) | [report](./docs/report.docx) |

Разработать приложение на базе **JavaServer Faces Framework**, которое осуществляет проверку попадания точки в заданную область на координатной плоскости.

Приложение должно включать в себя **2 facelets-шаблона** - _стартовую страницу_ и _основную страницу приложения_, а также набор управляемых бинов (`managed beans`), реализующих логику на стороне сервера.

<img alt="Areas" src="./.resources/areas.png" height="350">

### Стартовая страница должна содержать следующие элементы:

- "Шапку", содержащую ФИО студента, номер группы и номер варианта.
- Интерактивные часы, показывающие текущие дату и время, обновляющиеся раз в **8 секунд**.
- Ссылку, позволяющую перейти на основную страницу приложения.

### Основная страница приложения должна содержать следующие элементы:

- Набор компонентов для задания координат точки и радиуса области в соответствии с вариантом задания. Может потребоваться использование дополнительных библиотек компонентов - [ICEfaces](https://www.icesoft.com/icefaces/) (префикс `"ace"`) и [PrimeFaces](https://www.primefaces.org/) (префикс `"p"`). Если компонент допускает ввод заведомо некорректных данных (таких, например, как буквы в координатах точки или отрицательный радиус), то приложение должно осуществлять их валидацию.
- Динамически обновляемую картинку, изображающую область на координатной плоскости в соответствии с номером варианта и точки, координаты которых были заданы пользователем. Клик по картинке должен инициировать сценарий, осуществляющий определение координат новой точки и отправку их на сервер для проверки её попадания в область. Цвет точек должен зависеть от факта попадания / непопадания в область. Смена радиуса также должна инициировать перерисовку картинки.
- Таблицу со списком результатов предыдущих проверок.
- Ссылку, позволяющую вернуться на стартовую страницу.

### Дополнительные требования к приложению:

- Все результаты проверки должны сохраняться в базе данных под управлением **СУБД Oracle**. 
- Для доступа к БД необходимо использовать **ORM Hibernate**. 
- Для управления списком результатов должен использоваться `Session-scoped Managed Bean`. 
- Конфигурация **управляемых бинов** должна быть задана с помощью параметров в **конфигурационном файле**. 
- **Правила навигации** между страницами приложения должны быть заданы в отдельном **конфигурационном файле**.

### Вопросы к защите лабораторной работы:

**Ответы**: [*новые*](https://github.com/EgorMIt/ITMO/blob/master/2%20-%20%D0%92%D0%B5%D0%B1-%D0%9F%D1%80%D0%BE%D0%B3%D1%80%D0%B0%D0%BC%D0%BC%D0%B8%D1%80%D0%BE%D0%B2%D0%B0%D0%BD%D0%B8%D0%B5/Lab3.md) и [*старые*](https://github.com/AppLoidx/Web-Development-Cheats/blob/master/itmo-university/labs/Lab3.md)

1. Технология **JavaServer Faces**. Особенности, отличия от сервлетов и **JSP**, преимущества и недостатки. Структура **JSF**-приложения. 
2. Использование **JSP**-страниц и **Facelets**-шаблонов в **JSF**-приложениях. 
3. **JSF**-компоненты - особенности реализации, иерархия классов. Дополнительные библиотеки компонентов. Модель обработки событий в **JSF**-приложениях. 
4. Конвертеры и валидаторы данных. 
5. Представление страницы **JSF** на стороне сервера. Класс `UIViewRoot`. 
6. Управляемые бины - назначение, способы конфигурации. Контекст управляемых бинов. 
7. Конфигурация **JSF**-приложений. Файл `faces-config.xml`. Класс `FacesServlet`. 
8. Навигация в **JSF**-приложениях. 
9. Доступ к БД из Java-приложений. Протокол **JDBC**, формирование запросов, работа с драйверами СУБД. 
10. Концепция **ORM**. Библиотеки **ORM** в приложениях на Java. Основные API. Интеграция **ORM**-провайдеров с драйверами **JDBC**. 
11. Библиотеки `ORM Hibernate` и `EclipseLink`. Особенности, API, сходства и отличия. 
12. Технология **JPA**. Особенности, API, интеграция с ORM-провайдерами.

### Как запустить?

#### Helios

[Гайд](https://github.com/AppLoidx/Web-Development-Cheats/blob/master/itmo-university/%D0%94%D0%B5%D0%BF%D0%BB%D0%BE%D0%B8%D0%BC%202%20%D0%BB%D0%B0%D0%B1%D1%83%20%D0%BD%D0%B0%20helios%2C%20%D0%B8%D1%81%D0%BF%D0%BE%D0%BB%D1%8C%D0%B7%D1%83%D1%8F%20WildFly.md) по деплою на Helios в `WildFly`.

#### Локально

Как на Helios, но локально :grin:

## Лицензия <a name="license"></a>

Проект доступен с открытым исходным кодом на условиях [Лицензии MIT](https://opensource.org/licenses/MIT).
*Авторские права 2023 Max Barsukov*

**Поставьте звезду :star:, если вы нашли этот проект полезным.**
