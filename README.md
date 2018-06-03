# Описание

Данная сборка поможет вам быстро развернуть «1С-Битрикс: Веб-окружение» на вашем компьютере из под любой системы. При установке виртуальной машины будет скачан vagrant box https://app.vagrantup.com/centos/boxes/7 , а также поставлены следующие программы: wget, nano, composer и BitrixVM v7.x. Для корректной установки вам потребуется установленная программа Vagrant последней версии, скачать ее можно по ссылке https://www.vagrantup.com/downloads.html. Также вам понадобиться программа виртуализации VirtualBox - https://www.virtualbox.org/wiki/Downloads. 


# Установка

После клонирования репозитория на ваш компьютер откройте консоль и перейдите в папку `Путь_до_репозитория/vagrant/`. Находясь в данной папке выполните команду `vagrant up` и дождитесь окончания усутановки. Если во время установки у вас появилось следующее сообщение `vagrant-reload is not installed! Please install it and try again.`, то вам необходимо установить плагин `vagrant-reload` с помощью команды: `vagrant plugin install vagrant-reload`. После установки системы откройте в браузере uri: `http://127.0.0.1:8888/` и установите необходимую версию 1С-Битрикс. Для подключения к базе данных используйте хост `http://127.0.0.1:8889` , логин - `root`, пароль - `bitrix`. Все что располагается в корне вашего проекта, включая папку `vagrant` будет моментально синхронизироваться с папкой `/home/bitrix/` на виртуальной машине.

# Полезные команды vagrant 

Все команды `vagrant` необходимо производить там, где располагается файл `vagrant/VagrantFile`.

`vagrant halt` - Остановка виртуальной машины (рекомендуемый способ).

`vagrant up` - При первом запуске будет запущена инициализация виртуальной машины, далее машина будет просто влключаться.

`vagrant reload` - Перезагрузка виртуальной машины.

`vagrant reload --provision` - Пересоздание виртуальной машины. Файлы и папки из вашей физической мышины затронуты не будут, более того после пересоздания ваш сайт и вся его структура останутся невредимыми.

`vagrant destroy` - Удаление виртуальной машины.

`vagrant --help` - Вывод списка команд.

# Дополнительно

Более подробную информацию по работе с «1С-Битрикс: Веб-окружение» вы можете найти по ссылке - https://dev.1c-bitrix.ru/learning/course/?COURSE_ID=37&CHAPTER_ID=08809&LESSON_PATH=3908.8809
