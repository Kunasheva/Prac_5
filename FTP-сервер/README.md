FTP сервер
Цель работы - Научиться программно работать с файлами и файловой системой, читать, создавать, перемещать и передавать файлы по сети 
Задания для выполнения 
Создать сервер, который предоставляет клиенту базовые возможности файлового менеджера по сети. Клиент после подключения к серверу должен иметь возможности просматривать список файлов и папок в рабочей директории сервера (рабочая директория - это специальная папка, к которой имеет доступ процесс сервера, но она отделена от парки с кодом сервера и от любых системных файлов), создавать и удалять в ней папки, создавать, копировать и переименовывать файлы. Также клиент может передать на сервер название и содержимое файла и сервер должен создать соответствующий файл в текущей директории. Кроме того, клиент может запросить содержимое любого файла и сервер должен передать его в ответ. 
Дополнительные задания: 
- Ограничьте возможности пользователя рамками одной определенной директории. Внутри нее он может делать все, что хочет: создавать и удалять любые файлы и папки. Нужно проследить, чтобы пользователь не мог совершить никаких действий вне пределов этой директории. Пользователь, в идеале, вообще не должен догадываться, что за пределами этой директории что-то есть. 
- Добавьте логирование всех действий сервера в файл. Можете использовать разные файлы для разных действий, например: подключения, авторизации, операции с файлами. 
- Добавьте возможность авторизации пользователя на сервере. 
- Добавьте возможность регистрации новых пользователей на сервере. При регистрации для пользователя создается новая рабочая папка (проще всего для ее имени использовать логин пользователя) и сфера деятельности этого пользователя ограничивается этой папкой. Реализуете квотирование дискового пространства для каждого пользователя. 
- Реализуйте учётную запись администратора сервера. Напишите отладочный клиент. Клиент должен подключаться к серверу и в автоматическом режиме тестировать корректность его работы. Используйте подход, аналогичный написанию модульных тестов. Клиент должен вывести предупреждающее сообщение, если сервер работает некорректно.

Подключение клиента к серверу:
клиент:
![image](https://user-images.githubusercontent.com/90391164/146363743-dcc337c5-46ef-4db4-9373-2688ed0ac78b.png)
сервер:
![image](https://user-images.githubusercontent.com/90391164/146363801-329b8c9e-e591-44c7-8f5c-5399e9c0a6f9.png)

Создалась папка с логином:
![image](https://user-images.githubusercontent.com/90391164/146363912-6b0a2fc6-aca6-4c2b-b489-55ab48a54e68.png)

Создадим в ней папку:
![image](https://user-images.githubusercontent.com/90391164/146364031-a89dffde-70b7-4bb6-9b55-6ee0214d7950.png)
![image](https://user-images.githubusercontent.com/90391164/146364052-ed8d9f11-b0ce-4515-93bf-53f18d214fa0.png)

так наши действия показаны в сервере:
![image](https://user-images.githubusercontent.com/90391164/146364127-107e5d7a-7f03-43fa-aaa4-c09cb1ce6cc8.png)

создание файла командой echo:

![image](https://user-images.githubusercontent.com/90391164/146364662-84f095c4-07d6-4a00-90ea-d34b56b605ef.png)

проверим его наличие и содержимое:
![image](https://user-images.githubusercontent.com/90391164/146364792-7df8d065-c4b9-4f8c-b0aa-67f44acea224.png)
![image](https://user-images.githubusercontent.com/90391164/146364805-f29b6e42-61f1-4f2c-921b-9c4b2eeb9927.png)

проверим содержимое папки first командой ls:
![image](https://user-images.githubusercontent.com/90391164/146364862-06666d11-ecb9-49c7-ab4e-ab742a984372.png)

Выведем содержимое файла командой cat:
![image](https://user-images.githubusercontent.com/90391164/146364978-e69aad39-65a6-43c6-a2b8-d147dd395e40.png)

Перемещение:
![image](https://user-images.githubusercontent.com/90391164/146365043-7295d2b7-88bb-47ed-94b5-a73db9a1a84b.png)

удаление файла командой rm:
![image](https://user-images.githubusercontent.com/90391164/146365509-6e9ea16b-3294-4462-99b5-e3d37f225c6e.png)

Создание и удаление папки:
команда rmdir
![image](https://user-images.githubusercontent.com/90391164/146365692-34662337-07c1-4bc5-8192-d495b770070b.png)

Выход с помощью exit:
как показано в консоли:
![image](https://user-images.githubusercontent.com/90391164/146365969-8a3d6db7-6084-4689-a3ec-3874e7875fa3.png)



Дополнительные задания: Ограничьте возможности пользователя рамками одной определенной директории. Внутри нее он может делать все, что хочет: создавать и удалять любые файлы и папки. Нужно проследить, чтобы пользователь не мог совершить никаких действий вне пределов этой директории. Пользователь, в идеале, вообще не должен догадываться, что за пределами этой директории что-то есть.

![image](https://user-images.githubusercontent.com/90391164/146366453-3a3eb6ec-3777-4e11-85b8-03a6d5fdb6b3.png)
проверили
Добавьте логирование всех действий сервера в файл. Можете использовать разные файлы для разных действий, например: подключения, авторизации, операции с файлами.

Логи добавляются в файл log.txt
![image](https://user-images.githubusercontent.com/90391164/146366709-a0b434d6-ba1f-44cb-9a62-88fc1ea02ef7.png)
Добавьте возможность авторизации пользователя на сервере.

Если пользователь уже зарегистрирован и хочет войти под своим именем - ( авторизоваться), он должен ввести цифру 2, затем ввести пароль - ( как на скриншоте ниже - файл клиента)

![image](https://user-images.githubusercontent.com/90391164/146366750-5c7af439-d22e-46cb-bbbd-ce7edecf6d0f.png)

Данные зарегестрированных пользователей сохраняем в users.txt
![image](https://user-images.githubusercontent.com/90391164/146366887-ae4f06c8-64b1-4774-b008-cd274fc65f14.png)

Добавьте возможность регистрации новых пользователей на сервере. При регистрации для пользователя создается новая рабочая папка (проще всего для ее имени использовать логин пользователя) и сфера деятельности этого пользователя ограничивается этой папкой.

ввести цифру 1 при входе
![image](https://user-images.githubusercontent.com/90391164/146363743-dcc337c5-46ef-4db4-9373-2688ed0ac78b.png)

информация при регистрации сохраняется в users.txt
Реализуйте учётную запись администратора сервера.
![image](https://user-images.githubusercontent.com/90391164/146367204-9f79834f-78e9-42ad-bc1f-e24be35b1022.png)
