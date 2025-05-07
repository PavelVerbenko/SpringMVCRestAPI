Проект представляет собой простое CRUD-приложение на Spring Framework для управления списком пользователей (Person). Основные цели:

- Демонстрация работы с Spring MVC, JDBC, валидацией данных и шаблонизатором Thymeleaf.

- Реализация базовых операций: создание, чтение, обновление, удаление записей в PostgreSQL.

СТЭК: Java, Spring MVC, Spring JDBC, Thymeleaf, HTML, PostgreSQL.


| Класс                   | Описание                                                                                                                 |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------|
| SpringConfig.java      | Конфигурация Spring: настройка БД, Thymeleaf, компонентов приложения.   Создает DataSource, JdbcTemplate, шаблонизаторы. |
| Person.java    | Модель данных с валидацией полей (аннотации @NotEmpty, @Size, @Min).                                                     |
| PersonDAO.java          | Взаимодействие с БД через JdbcTemplate (SQL-запросы).                                                                    |
| PeopleController.java       | Контроллер: обработка HTTP-запросов (GET/POST/PATCH/DELETE), передача данных в представления.                            |
|PersonMapper.java      | Преобразует строки ResultSet в объекты Person.                                                                           |
| MySpringMvcDispatcherServletInitializer.java | Инициализация Spring MVC и настройка фильтров (например, для поддержки PATCH/DELETE).                                    |
HTML-шаблоны (index.html, new.html, edit.html) | Представления на Thymeleaf: отображение списка пользователей, форм создания/редактирования.                              
