# Домашнее задание к занятию «Основы Git»

## Задание №1. Знакомимся с GitLab (обязательно) и bitbucket (по желанию)

### Gitlab

Создадим аккаунт в Gitlab, если у вас его еще нет:
1. Gitlab. Для [регистрации](https://gitlab.com/users/sign_up)  можно использовать 
аккаунт google, github и другие. 
2. После регистрации или авторизации в gitlab создайте новый проект, нажав на ссылку `Create a projet`. 
Желательно назвать также, как и в гитхабе `devops-netology` и `visibility level` выбрать `Public`.
3. Галочку `Initialize repository with a README` луше не ставить, чтобы не пришлось разрешать конфликты.
4. Если вы зарегистрировались при помощи аккаунта в другой системе и не указали пароль, то увидите сообщение
`You won't be able to pull or push project code via HTTPS until you set a password on your account`. 
Тогда перейдите по [ссылке](https://gitlab.com/profile/password/edit) из этого сообщения и задайте пароль. 
Если вы уже умеете пользоваться ssh ключами, то воспользуйтесь этой возможностью (подробнее про ssh мы поговорим в следующем учебном блоке).
5. Перейдите на страницу созданного вами репозитория, url будет примерно такой:
https://gitlab.com/YOUR_LOGIN/devops-netology и изучите предлагаемые варианты для начала работы в репозитории в секции
`Command line instructions`. 
6. Запомните вывод команды `git remote -v`.
7. В связи с тем, что это будет наш дополнительный репозиторий, ни один вариант из перечисленных в инструкции (на странице 
вновь созданного репозитория) нам не подходит. Поэтому добавляем этот репозиторий как дополнительный `remote` к созданному
репозиторию в рамках предыдущего домашнего задания:
`git remote add gitlab https://gitlab.com/YOUR_LOGIN/devops-netology.git`.
8. Отправьте изменения в новый удалённый репозиторий `git push -u gitlab main`.
9. Обратите внимание как изменился результат работы команды `git remote -v`.

[![Screenshot_43.png](https://s.iimg.su/s/29/pRo4iC4mobPvKXzTMxKjFCLWZtQpSDz2kz1kSCqp.png)](https://iimg.su/i/LB4WJY)

## Задание №2. Теги

Представьте ситуацию, когда в коде была обнаружена ошибка - надо вернуться на предыдущую версию кода,
исправить ее и выложить исправленный код в продакшн. Мы никуда код выкладывать не будем, но пометим некоторые коммиты тегами и 
создадим от них ветки. 

1. Создайте легковестный тег `v0.0` на HEAD коммите и запуште его во все три добавленных на предыдущем этапе `upstream`.
2. Аналогично создайте аннотированный тег `v0.1`.
3. Перейдите на страницу просмотра тегов в гитхабе (и в других репозиториях) и посмотрите, чем отличаются созданные теги. 
 
 
[![Screenshot_44.png](https://s.iimg.su/s/29/ZsJNrw4iCsOaEfhMZpmCRLUeyIjnusHbQtvsCrAE.png)](https://iimg.su/i/vfUg8Y)

 
## Задание №3. Ветки 

Давайте посмотрим, как будет выглядеть история коммитов при создании веток. 

1. Переключитесь обратно на ветку `main`, которая должна быть связана с веткой `main` репозитория на `github`.
2. Посмотрите лог коммитов и найдите хеш коммита с названием `Prepare to delete and move`, который был создан в пределах предыдущего домашнего задания. 
3. Выполните `git checkout` по хешу найденного коммита. 
4. Создайте новую ветку `fix` базируясь на этом коммите `git switch -c fix`.
5. Отправьте новую ветку в репозиторий на гитхабе `git push -u origin fix`.
6. Посмотрите, как визуально выглядит ваша схема коммитов: https://github.com/YOUR_ACCOUNT/devops-netology/network. 
7. Теперь измените содержание файла `README.md`, добавив новую строчку.
8. Отправьте изменения в репозиторий и посмотрите, как изменится схема на странице https://github.com/YOUR_ACCOUNT/devops-netology/network 
[![Screenshot_45.png](https://s.iimg.su/s/29/jKWIXDqVvDZiXnmqLbfnuQwrhGmnzILfZRxtRutr.png)](https://iimg.su/i/IQlyr3)


[![Screenshot_46.png](https://s.iimg.su/s/29/XyKwA7GFyMwKobhZHbyAyiJMW7rAhMKgq0n8TIme.png)](https://iimg.su/i/ExYPkZ)

## Задание №4. Упрощаем себе жизнь

Давайте попробуем поработь с Git при помощи визуального редактора. 

1. В используемой нами IDE Py Charm откройте визуальный редактор работы с git, находящийся в меню View -> Tool Windows -> Git.
2. Измените какой-нибудь файл, и он сразу появится на вкладке `Local Changes`, отсюда можно выполнить коммит нажав на кнопку внизу этого диалога. 
3. Элементы управления для работы с гитом будут выглядеть примерно вот так:
   ![Работа с гитом](img/ide-git-01.jpg)
4. Попробуйте выполнить пару коммитов используя IDE. 
https://www.jetbrains.com/help/pycharm/commit-and-push-changes.html – здесь можно найти справочную информацию по визуальному интерфейсу. 
И если вверху экрана выбрать свою операционную систему, то можно посмотреть горячие клавиши для работы с гитом. 
Подробней о визуальном интерфейсе будет рассказано на одной из следующих лекций.

[![Screenshot_47.png](https://s.iimg.su/s/29/WyErirnE44ftujvXwfwFfYtmEQyMJsPltcAcV96W.png)](https://iimg.su/i/uM3Hfx)

[![Screenshot_48.png](https://s.iimg.su/s/29/2taeUxjz4FhFlhuC7T2RoM3iE0OgwseUVgxuqPFa.png)](https://iimg.su/i/7wsbaO)


*В качестве результата работы по всем заданиям приложите ссылки на ваши репозитории в github, gitlab и bitbucket*.  

*Прилагаю:*

```
https://github.com/skboyinboxru/devops-netology/tree/main
https://gitlab.com/skboyinboxru-group/devops-netology/-/tree/main?ref_type=heads

```
