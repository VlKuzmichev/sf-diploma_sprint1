# sf_diploma_sprint1
## _by Kuzmichev Vladislav_

Разворачиваем инфраструктуру в яндекс облаке:

> Клонируем проект

```sh
$ git clone https://github.com/VlKuzmichev/sf-diploma_sprint1
$ cd sf-diploma_sprint1
```

> Генерируем ключи и копируем в каталог проекта

```sh
$ ssh-keygen -t rsa
$ cp ~/.ssh/id_rsa* ./
```

> Правим реквизиты Yandex Cloud в файле terraform/main.tf 

```sh
$ cd terraform 
$ terraform init 
$ terraform apply
```

> Устанавливаем необходимые ингридиенты

```sh
$ cd ../ansible 
$ ansible-playbook -i ../inventory.ini -u ubuntu ansible_playbook.yml
```

В результате выполнения команд будет создан набор серверов.

Готово.
