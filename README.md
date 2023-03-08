# 2lab
## Homework

### Part I

1. Создайте пустой репозиторий на сервисе github.com (или gitlab.com, или bitbucket.com).

2. Выполните инструкцию по созданию первого коммита на странице репозитория, созданного на предыдещем шаге.
![image](https://github.com/lepeha81/2lab/blob/main/1.PNG)
![image](https://github.com/lepeha81/2lab/blob/main/2.PNG)
![image](https://github.com/lepeha81/2lab/blob/main/3.PNG)
![image](https://github.com/lepeha81/2lab/blob/main/4.PNG)

get init - создание пустого локального репозитория\
git remote add origin ... - добавление удаленного репозитория и присвоение ему названия\
git pull origin main - синхронизация с удалённым репозиторием\


3. Создайте файл `hello_world.cpp` в локальной копии репозитория (который должен был появиться на шаге 2). Реализуйте программу **Hello world** на языке C++ используя плохой стиль кода. Например, после заголовочных файлов вставьте строку `using namespace std

4. Добавьте этот файл в локальную копию репозитория.

5. Закоммитьте изменения с *осмысленным* сообщением.
![image](https://github.com/lepeha81/2lab/blob/main/5.PNG)
![image](https://github.com/lepeha81/2lab/blob/main/6.PNG)
![image](https://github.com/lepeha81/2lab/blob/main/7.PNG)
git status - просмотр текущих изменений\
git add - добавить файл в локальный репозиторий\
git config --global user.email - настройка адреса электронной почты\
git commit -m - описание коммита в локальном репозитории\
git push - отправка изменений в удалённый репозиторий\

6. Изменитьте исходный код так, чтобы программа через стандартный поток ввода запрашивалось имя пользователя. А в стандартный поток вывода печаталось сообщение `Hello world from @name`, где `@name` имя пользователя.
7. Закоммитьте новую версию программы. Почему не надо добавлять файл повторно `git add`?
![image](https://github.com/lepeha81/2lab/blob/main/8.PNG)
git commit -a -m - добавление файла в локальный репозиторий и закоммитирование его\

8. Запуште изменения в удалёный репозиторий.
![image](https://github.com/lepeha81/2lab/blob/main/9.PNG)

9. Проверьте, что история коммитов доступна в удалёный репозитории.
![image](https://github.com/lepeha81/2lab/blob/main/10.PNG)

git log - просмотр истории изменений

### Part II

**Note:** *Работать продолжайте с теми же репоззиториями, что и в первой части задания.*
1. В локальной копии репозитория создайте локальную ветку `patch1`.

![image](https://github.com/lepeha81/2lab/blob/main/13.PNG)

git checkout -b - переключение ветвей

2. Внесите изменения в ветке `patch1` по исправлению кода и избавления от `using namespace std`.
3. **commit**, **push** локальную ветку в удалённый репозиторий.
![image](https://github.com/lepeha81/2lab/blob/main/11.PNG)
4. Проверьте, что ветка `patch1` доступна в удалёный репозитории.

5. Создайте pull-request `patch1 -> master`.
![image](https://github.com/lepeha81/2lab/blob/main/14.PNG)

6. В локальной копии в ветке `patch1` добавьте в исходный код комментарии.
![image](https://github.com/lepeha81/2lab/blob/main/15.PNG)

7. **commit**, **push**.
![image](https://github.com/lepeha81/2lab/blob/main/16.PNG)
![image](https://github.com/lepeha81/2lab/blob/main/17.PNG)
8. Проверьте, что новые изменения есть в созданном на **шаге 5** pull-request
![image](https://github.com/lepeha81/2lab/blob/main/18.PNG)

9. В удалённый репозитории выполните  слияние PR `patch1 -> master` и удалите ветку `patch1` в удаленном репозитории.

10. Локально выполните **pull**.

![image](https://github.com/lepeha81/2lab/blob/main/19.PNG)

11. С помощью команды **git log** просмотрите историю в локальной версии ветки `master`.

![image](https://github.com/lepeha81/2lab/blob/main/20.PNG)

12. Удалите локальную ветку `patch1`.

![image](https://github.com/lepeha81/2lab/blob/main/21.PNG)

git branch -d - удаление ветки\


### Part III

**Note:** *Работать продолжайте с теми же репоззиториями, что и в первой части задания.*
1. Создайте новую локальную ветку `patch2`.
2. Измените *code style* с помощью утилиты [**clang-format**](http://clang.llvm.org/docs/ClangFormat.html). Например, используя опцию `-style=Mozilla`.

![image](https://github.com/lepeha81/2lab/blob/main/23.PNG)

style=<string> - загрузка конфигурации стиля\
clang-format -i - форматирование файла на место\

3. **commit**, **push**, создайте pull-request `patch2 -> master`.

  ![image](https://github.com/lepeha81/2lab/blob/main/24.PNG)

4. В ветке **master** в удаленном репозитории измените комментарии, например, расставьте знаки препинания, переведите комментарии на другой язык.

5. Убедитесь, что в pull-request появились *конфликтны*.

  ![image](https://github.com/lepeha81/2lab/blob/main/25.PNG)

6. Для этого локально выполните **pull** + **rebase** (точную последовательность команд, следует узнать самостоятельно). **Исправьте конфликты**.
Нажал на исправление конфликт и убрал ошибки\

7. Сделайте *force push* в ветку `patch2`

  ![image](https://github.com/lepeha81/2lab/blob/main/26.PNG)

  git push -f удаляет из ветки на сервере все коммиты, которых нет в локальной версии, и записывает новые\
8. Убедитель, что в pull-request пропали конфликтны. 

9. Вмержите pull-request `patch2 -> master`.

  ![image](https://github.com/lepeha81/2lab/blob/main/27.PNG)
