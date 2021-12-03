# 03-sysadmin-01-terminal

5. 

Ресурсы по умолчанию:

RAM - 1024 MB

Processors - 2

Storage - 64 GB

6.

 Для изменения ресурсов RAM и CPU следует добавить в файл Varrantfile строки:

config.vm.provider "virtualbox" do |v|

  v.memory = X

  v.cpus = Y

end

8. 

Задать длину журнала history можно переменной HISTSIZE, строка man 669

   Директива ignoreboth для переменной HISTCONTROL указывает на то, что в списке истории не сохраняются как строки, начинающиеся с пробела (ignorespace), так и строки, соответствующие предыдущей записи в истории (ignoredups). 

9.

строка man 892

фигурные скобки применимы в сценарии сокращения команды при перечислении объектов

10.

touch testfile{1..100000}.txt

перед запуском требуется увеличить лимит на размер стека ulimit -s 32768 - иначе получим ошибку Argument list too long.

Аналогично и с touch testfile{1..300000}.txt

11.

конструкция [[ -d /tmp ]] возвращает 0 или 1 в зависимости от выражения внутри ( В данном случае возвращает Истину, т. к. выражение внутри проверяет существует директория  /tmp )

12.

vagrant@vagrant:~$ mkdir /tmp/new_path_directory/bash

vagrant@vagrant:~$ cp /bin/bash /tmp/new_path_directory/bash

vagrant@vagrant:~$ PATH=/tmp/new_path_directory/bash:$PATH

13.

команда at используется для назначения одноразового задания на заданное время, а команда batch — для назначения одноразовых задач, которые должны выполняться, когда загрузка системы становится меньше 0,8

