# Home_work_33.1_Test_Rostelekom
Task-33.1_PJ_04
Тестирование формы авторизации Личного кабинета Ростелеком

 В данном проекте предстоит протестировать новый интерфейс авторизации в личном кабинете от заказчика Ростелеком Информационные Технологии по предоставленным требованиям к сайту.

→ Объект тестирования: https://b2c.passport.rt.ru

Задание:

Протестировать требования. Разработать тест-кейсы (не менее 15). Необходимо применить несколько техник тест-дизайна. Провести автоматизированное тестирование продукта (не менее 15 автотестов). Заказчик ожидает по одному автотесту на каждый написанный тест-кейс. Оформить свой набор автотестов в GitHub. Оформить описание обнаруженных дефектов. Использовать шаблоны для оформления тест-кейсов и обнаруженных дефектов.

Выполнение проекта:

Протестированы требования и указаны комментарии/замечания по пунктам.
Разработаны тест-кейсы (более 20) с использованием шаблона.
Оформлено описание обнаруженных дефектов с использованием шаблона.
→ Ссылка на документ: https://docs.google.com/spreadsheets/d/1DTHy_Cq76tkPIw_IAawSbmnKgTq8FoPi/edit?usp=sharing&ouid=104994275562405797848&rtpof=true&sd=true

Проект выполнен с использованием: PageObject, Selenium и PyTest.

В корневой папке находятся файлы settings.py с тестовыми данными, msedgedriver.exe, requirements.txt для установки необходимых для тестирования библиотек.

Папка tests содержит файлы для запуска автотестов: test_auth_page.py - тесты для страницы авторизация, test_registr_page.py - тесты для страницы регистрация.

Папка pages содержит следующие файлы: locators.py - список локаторов на веб страницах, base_page.py - базовая страница, от которой унаследованы все остальные классы, auth_page.py - содержит класс для страницы авторизация, registr_page.py - содержит класс для страницы регистрация.

Перед запуском тестов требуется установить необходимые библиотеки командой:

pip install -r requirements.txt 

Запуск тестов при помощи команд в консоли:

 python -m pytest -v --driver Edge --driver-path msedgedriver.exe tests/test_auth_page.py
 python -m pytest -v --driver Edge --driver-path msedgedriver.exe tests/test_registr_page.py 
 
Сценарии проверок автотестами: Каждый тест внутри проекта содержит описание своего назначения.

Тестовые сценарии страницы авторизация (test_auth_page.py):

Проверка различных элементов страницы на их наличие и название согласно требованию. Проверка табов меню авторизация. При переходе по ссылкам "Забыл пароль" и "Зарегистрироваться" открываются соответствующие страницы. Проверка аутентификации пользователя с валидными и невалидными данными. 

Тестовые сценарии страницы регистрация (test_registr_page.py):

Проверка различных элементов страницы на их наличие и название согласно требованию. Сценарии регистрации пользователя с валидными данными ("Имя" и "Фамилия" - буквы кириллицы либо тире). Сценарии регистрации пользователя с данными, которы были использованы ранее. Проверки полей ввода валидными и невалидными данными.
