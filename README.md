- [VCS](#vcs)
- [Работа с консолью](#работа-с-консолью)
- [Навигация](#навигация)
- [Работа с файлами и папками](#работа-с-файлами-и-папками)
    - [Создание](#создание)
    - [Копирование и перемещение](#копирование-и-перемещение)
    - [Чтение](#чтение)
    - [Удаление](#удаление)
- [Полезные возможности](#полезные-возможности)
- [Работа с GIT-ом](#работа-с-GIT-ом)
    - [Чем отличается запоминание от сохранения?](#чем-отличается-запоминание-от-сохранения)
    - [Генерация пары SSH ключей](#генерация-пары-SSH-ключей)
    - [Markdown](#Markdown)
- [Статусы файлов в Git](#Статусы-файлов-в-Git)
- [Порядок создания проекта на GitHub](#порядок-создания-проекта-на-GitHub)


## VCS
Система контроля версий, или VCS, — это программное обеспечение, которое помогает отслеживать изменения в программах, текстовых файлах, больших документах, веб-сайтах и так далее.

- Система контроля версий, или VCS (SCM), — программа, позволяющая контролировать изменения в проекте.
- Git — один из примеров системы контроля версий: он позволяет хранить, изменять и анализировать историю проекта.
- Git — незаменимый в команде инструмент, ведь он помогает объединять результаты работы нескольких человек.
- Чтобы Git начал отслеживать изменения в проекте, папку с файлами этого проекта нужно сделать Git-репозиторием (от англ. repository — «хранилище»).

Установка: https://practicum.yandex.ru/trainer/git-basics/lesson/2a82ddb7-19cf-437e-a187-f976804fddad/

## Работа с консолью:
- символ доллара ($) — он означает, что программа ждёт ваших команд.
- pwd (от англ. print working directory) — «показать рабочую папку». Узнать, где вы сейчас.
- ls – список файлов и папок в директории
- ls -a - вывели список, в котором отображаются скрытые файлы ., .. и .git. –a это –all
- ls -l (от англ. long). Команда ls -l будет выводить подробную информацию о содержимом текущего каталога.
- ls ~ - выведет содержимое домашней директории вне зависимости от того, что показывает pwd.
- ls .. - покажет содержимое родительской директории.
- cd ~ - вернуться в домашнюю директорию. С помощью терминала вы всегда можете перейти к домашней директории. Для этого нужно ввести команду cd (от англ. change directory — «сменить директорию») и символ ~ — обозначение домашней директории. 
- cd (от англ. change directory — «сменить директорию»). Допустим, вы находитесь в директории /projects. Если ввести команду cd github, она перенесёт вас в директорию /projects/github. если в названии папки есть пробелы, при вводе нужно использовать кавычки: $ cd "Фотографии с дня рождения"
- .. - чтобы вернуться в родительскую директорию — то есть на уровень выше, — вместо названия папки нужно написать две точки
- . – с точки начинаются названия скрытых файлов
- touch (англ. «коснуться») – чтобы создать файл, нужно ввести в консоль команду touch с именем файла в качестве параметра: touch %ИМЯ_ФАЙЛА% - $ touch my-new-file.
- mkdir (от англ. make directory — «создать директорию»). Можно создать целую структуру директорий одной командой с помощью флага –p: mkdir -p dir1/dir-inside/dir-deeper-inside # создали папку dir-deeper-inside в папке dir-inside, которая находится в папке dir1
- cp - (от англ. copy — «копировать»). Копирование файлов. $ cp что_копируем что_копируем что_копируем куда_копируем: $ cp index.html style.css script.js src/ - скопировали три файла (index.html, style.css и script.js) в папку src
- mv - перемещение файлов и папок. После имени команды указывают список файлов и папок, которые нужно переместить, а затем — папку, в которую нужно выполнить перемещение. $ mv table.csv ./very-important-files (./ - текущая директория)
- cat (от англ. concatenate and print — «объединить и распечатать») - прочитать файл. Команда распечатает то, что содержится в нём. Команда cat работает только с текстовыми файлами. Вывести этой командой файл другого типа (например, изображение) не получится.
- rm (от англ. remove — «удалить») - удалить файл. 
- rmdir (от англ. remove directory — «удалить директорию») - команда удалит папку. Если в папке, которую вы пытаетесь стереть, есть какие-то файлы, то командная строка не удалит её и выведет сообщение о том, что папка не пуста (англ. Directory not empty).
- rm -r (-r — от англ. recursive, «рекурсивный») рекурсивно удаляет файлы и папки. Это значит, что удаление будет последовательно применяться к каждому из элементов в этой папке — пока не сотрёт их все. Затем команда удалит пустую директорию.
- && - Команды в терминале необязательно вбивать и выполнять по очереди. Их можно указывать не по одной, а сразу списком. Для этого их нужно разделить двумя амперсандами (&&). $ mkdir second-project && cd second-project && touch index.html style.css - создаём папку second-project, переходим в папку second-project и создаём в ней два файла: index.html и style.css
- Tab - автоматически дописывает не только команды, но и пути. Начните печатать имя папки или файла (они должны быть в той же директории) и нажмите Tab. Терминал заполнит имя автоматически. Есть ещё один способ использовать Tab при навигации в другую директорию. Если ввести cd с названием папки, а затем нажать Tab, в консоль в качестве подсказки выведутся все возможные пути.
- cd /c + Enter - Чтобы попасть в корневую директорию Windows, нужно перейти на соответствующий диск.

## Навигация
- pwd (от англ. print working directory, «показать рабочую папку») — покажи, в какой я папке;
- ls (от англ. list directory contents, «отобразить содержимое директории») — покажи файлы и папки в текущей папке;
- ls -a — покажи также скрытые файлы и папки, названия которых начинаются с символа .;
- cd first-project (от англ. change directory, «сменить директорию») — перейди в папку first-project;
- ls -l (от англ. long). Команда ls -l будет выводить подробную информацию о содержимом текущего каталога.
- cd first-project/html — перейди в папку html, которая находится в папке first-project;
- cd .. — перейди на уровень выше, в родительскую папку;
- cd ~ — перейди в домашнюю директорию (/Users/Username);
- cd / — перейди в корневую директорию.
## Работа с файлами и папками
### Создание
- touch index.html (англ. touch, «коснуться») — создай файл index.html в текущей папке;
- touch index.html style.css script.js — если нужно создать сразу несколько файлов, можно напечатать их имена в одну строку через пробел;
- mkdir second-project (от англ. make directory, «создать директорию») — создай папку с именем second-project в текущей папке.
### Копирование и перемещение
- cp file.txt ~/my-dir (от англ. copy, «копировать») — скопируй файл в другое место;
- mv file.txt ~/my-dir (от англ. move, «переместить») — перемести файл или папку в другое место.
### Чтение
- cat file.txt (от англ. concatenate and print, «объединить и распечатать») — распечатай содержимое текстового файла file.txt.
### Удаление
- rm about.html (от англ. remove, «удалить») — удали файл about.html;
- rmdir images (от англ. remove directory, «удалить директорию») — удали папку images;
- rm -r second-project (от англ. remove, «удалить» + recursive, «рекурсивный») — удали папку second-project и всё, что она содержит.

## Полезные возможности
- Команды необязательно печатать и выполнять по очереди. Можно указать их списком — разделить двумя амперсандами (&&).
- У консоли есть собственная память — буфер с несколькими последними командами. По ним можно перемещаться с помощью клавиш со стрелками вверх (↑) и вниз (↓).
- Чтобы не вводить название файла или папки полностью, можно набрать первые символы имени и дважды нажать Tab. Если файл или папка есть в текущей директории, командная строка допишет путь сама.
Например, вы находитесь в папке dev. Начните вводить cd first и дважды нажмите Tab. Если папка first-project есть внутри dev, командная строка автоматически подставит её имя. Останется только нажать Enter.

## Работа с GIT-ом
Первым делом необходимо представиться. Чтобы участникам проекта было понятно, кто и какие изменения вносил, нужно представиться и указать имя пользователя и адрес электронной почты.
- git config (от англ. configuration — «конфигурация», «настройка») с ключом --global (англ. «глобальный»). В качестве значения user.name нужно указать своё имя или никнейм. Для настройки параметра user.email указывают электронную почту.
$ git config --global user.name "User Namovich" - имя или ник нужно написать латиницей и в кавычках
$ git config --global user.email username@yandex.ru - здесь нужно указать свой настоящий email
- $ cat ~/.gitconfig или $ git config --list - Все глобальные настройки Git хранит в файле .gitconfig в домашней директории. Команда запишет в этот файл указанные имя и почту. Чтобы убедиться в этом, можно вызвать команду для чтения файлов.
- git init - Сделать папку репозиторием. Например, создайте папку first-project и сделайте её Git-репозиторием: перейдите в неё с помощью команды cd и выполните git init.
- rm -rf .git - Если вы случайно сделали Git-репозиторием не ту папку, её можно «разгитить». Для этого нужно удалить скрытую подпапку .git. 
ключ -r (от англ. recursive — «рекурсивно») позволяет удалять папки вместе с их содержимым;
ключ -f (от англ. force — «заставить») избавит вас от вопросов вроде «Вы точно хотите удалить этот файл? А этот? И этот тоже?»
- git status - (от англ. status — «статус», «состояние») — она показывает текущее состояние репозитория.
- git add --all (от англ. add — «добавить» + от англ. all — «всё»). Ключ, или флаг, --all позволяет подготовить к сохранению все файлы в репозитории.
- git add todo.txt - Добавлять файлы можно и по одному, без ключа --all.
- git add . - Также можно добавить текущую папку целиком — в этом случае все файлы в ней тоже будут добавлены. Обратиться к текущей папке в Bash позволяет точка (.).
- git commit -m ‘Мой первый коммит!’ - Сделать коммит можно командой git commit c ключом -m (от англ. message — «сообщение»), который присваивает коммиту сообщение.
- git log - Просмотреть историю коммитов
- git push - Отправить изменения на удалённый репозиторий. В первый раз эту команду нужно вызвать с флагом -u и параметрами origin (имя удалённого репозитория) и main или master (название текущей ветки). Флаг -u свяжет локальную ветку с одноимённой удалённой. Как вы связывали локальный и удалённый репозитории в предыдущем уроке, так же и здесь нужно дополнительно связать ветки - $ git push -u origin master.
- README.md — текстовый файл, который можно создать командой touch, а затем редактировать так же, как и любой другой текстовый документ. Например, в блокноте.
- хеш - информация о коммите. Это набор данных: когда был сделан коммит, содержимое файлов в репозитории на момент коммита и ссылка на предыдущий, или родительский (англ. parent), коммит. Все хеши и таблицу хеш → информация о коммите Git сохраняет в служебные файлы. Они находятся в скрытой папке .git в репозитории проекта.

### Чем отличается запоминание от сохранения?
Команда git add не сохраняет содержимое файлов в репозитории. Само сохранение, или фиксацию состояния файлов, называют коммитом (от англ. commit — «совершать», «фиксировать»). «Сделать коммит» значит сохранить текущую версию файла. 
Если провести аналогию, команду git add можно сравнить с добавлением товаров в корзину в интернет-магазине, а коммит — с оформлением и оплатой заказа.

### Генерация пары SSH ключей
https://practicum.yandex.ru/trainer/git-basics/lesson/42435683-0922-4231-bfb4-d7d32d61f50a/

### Markdown 
это специальный язык разметки. Он позволяет красиво отформатировать текстовый документ README.md.
https://skillbox.ru/media/code/yazyk-razmetki-markdown-shpargalka-po-sintaksisu-s-primerami/
https://gist.github.com/fomvasss/8dd8cd7f88c67a4e3727f9d39224a84c

## Статусы файлов в Git
- untracked - статусом untracked помечается файл, о существовании которого Git знает, но не следит за изменениями в нём. Этот статус — противоположность tracked, в который попадают все файлы, отслеживаемые Git.
- staged - файл переходит в статус staged после выполнения git add.
- modified - статус modified означает, что файл был изменён.

https://practicum.yandex.ru/trainer/git-basics/lesson/860e0bf4-ebd6-4e13-87fa-f76d92cfd11f/

## Порядок создания проекта на GitHub
1) Создать папку в любом месте на компьютере привычным способом или с помощью консоли ($ mkdir dir1) и перейти в нее
2) Сделать папку репозиторием (хранилищем) ($ git init) и проверить его состояние ($ git status)
3) Поместить в репозиторий файлы проекта и файл описания README.md
4) Представиться и указать имя пользователя и адрес электронной почты.
$ git config --global user.name "User Namovich"
$ git config --global user.email username@yandex.ru
5) Проверить, что имя и почта сохранились правильно ($ git config --list)
6) Создать удалённый репозиторий на GitHub, чтобы в будущем связать его с локальным. Название удалённого репозитория необязательно должно совпадать с именем папки проекта у вас на компьютере. Но чтобы не путаться, будем называть их одинаково.
7) Создать и привязать SSH-ключ к GitHub
8) Привязать удалённый репозиторий к локальному ($ git remote add origin git@github.com:%ИМЯ_АККАУНТА%/first-project.git) origin – переменная, которая содержит путь репозитория. Переменная используется, чтобы не вводить путь каждый раз заново при использовании в командах. Например: git pull origin master - в текущую локальную ветку залить из удаленного репозитория ветку master
9) Убедиться, что репозитории связаны (git remote -v)
10) Отметить файлы за изменением которых необходимо следить (поместить товары в корзину, подготовить файлы к коммиту) Все - $ git add –-all или по одному $ git add file.txt
11) Выполнить коммит ($ git commit -m ‘Мой первый коммит!’)
12)	Отправить изменения на удалённый репозиторий. Если это происходит первый раз, то команда - $ git push -u origin master. Флаг -u свяжет локальную ветку с одноимённой удалённой. Последующие раз команда - $ git push
13)	Зайти в репозиторий на GitHub и убедиться, что в репозитории появились файлы с изменениями.

https://practicum.yandex.ru/trainer/git-basics/lesson/1add1d42-16f2-4df3-b230-d3362e10acb8/