
## Инструкция по работе с 
Testing 

## Что такое Git?
Git - одна из реализации распределенных систем контроля версии, позволяющая организовать версионность, как локально, так и на удаленном. Самая популярная платформа, реализущая *Git*, - [GitHub](https://github.com)

## Подготовка репозитория
для создание в папке репозитория необходимо открыть эту папку в терминале и написать команду *git init*, после чего в этой папке создатся скрытая папка *git*, и таким образом папка станет репозиторием. Testing

## Создание коммитов

### Просмотр состояния репозитория
Для просмотра состояния репозитория используется команда *git status*.  В терминале с открытой папкой-репозиторием неопходимо написать команду *git status*. В результате можно увидеть следующее выводы:
1. On branch *** nothing to commit - это озночает нет активных изменений
2. Untracked file - это озночает, что имеются файлы, не отслеживаемые системой контроля версий

### Добавление файла к "коммиту"
Для того, чтобы добавить файл к "сохранению", необходимо использовать команду *git add*. В терминале с открытой папкой-репозиторием необходимо написать *git add <название файла>* , и этот файл к "сохранению" 

### Создание фиксаций
Для создания фиксации используется команда *git commit* . Для этого в терминале с папкой-репозиторием необходимо написать команду *git commit -m <сообщение к коммиту>*. Сообщение к коммиту писать **ОБЯЗАТЕЛЬНО** .

## Журнал изменений
Для просмотра историй изменений используется команда  *git log*. Для этого в терминале с папкой-репозиторием необходимо написать *git log*, и Вы увидете список всех коммитов в этой папке с описанием: имени, электронной почты, сообщением к коммиту и номер коммита.

## Перемещение между "коммитами"
Для перемещения между коммитами исползуется команда *git checkout*. Для этого в терминале с папкой-репозиторием необходима написать *git checkout <номер коммита>* . Номер коммита берется из журнала изменений ветки.


## Ветки в git

Ветки нужны для того, чтобы программисты могли вести совместную работу над проектом и не мешать друг другу при этом. При создании проекта, Git создает базовую ветку. Она называется master веткой.
Создать ветку можно командой *git branch*. Делать это надо в папке с репозиторием: *git branch <название новой ветки>*
Если у нас несколько версий черновика, мы можем вывести на экран ветку, где находимся, командой *git branch*.
Если потребуется переключиться с одной ветки на другую, вызовем команду *git checkout* <имя ветки>*

## Слияние веток и решение конфликтов

Допустим, черновики нас полностью устраивают и нам нужно внести изменения, чтобы информация появилась в чистовике. Для этого есть команда *git merge*.
Чтобы слить любую ветку с текущей, вызываем *git merge <имя ветки для слияния с текущей>*
### Конфликт изменений
При работе в двух ветках одновременно может возникнуть ситуация, когда в одной и другой ветке мы по-разному изменили блок текста. Если затем мы попробуем слить эти ветки, Git сообщит о конфликте и предложит выбрать, какие же изменения записать. 
Поэтому у проекта в репозитории должен быть один ответственный пользователь, наделённый правом проводить слияния и разрешать конфликты.

## Удаление веток
После слияние ветки и если она больше не нужна, ее можно удалить. Для этого необходимо указать *git branch -d <имя ветки которую надо удалить>* .

## Визуализация всех веток
*git log  --graph*
 Ключ -**graf** в связке с командой **log** позволяет отобразить коммиты в виде дерева.



