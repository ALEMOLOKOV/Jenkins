# Jenkins

## Подготовка к выполнению

1. Создать два VM: для jenkins-master и jenkins-agent.
![VMs](https://github.com/ALEMOLOKOV/Jenkins/assets/109212419/87675767-90bf-4d38-8aed-36030c05b5ca)

2. Установить Jenkins при помощи playbook.
![2](https://github.com/ALEMOLOKOV/Jenkins/assets/109212419/f22fd5ab-9074-4ddb-ab9d-a0bcd52a76d4)

3. Запустить и проверить работоспособность.

![jenkin sready](https://github.com/ALEMOLOKOV/Jenkins/assets/109212419/a3ae8ab1-c16e-4c0e-96c2-e770747caa2a)

4. Сделать первоначальную настройку.
![jenkins menu](https://github.com/ALEMOLOKOV/Jenkins/assets/109212419/c28833a4-e260-46cf-9575-0685c94ce190)

![STATUS](https://github.com/ALEMOLOKOV/Jenkins/assets/109212419/2356623f-d673-4ae9-b074-e12f22ee7bd6)


## Основная часть

1. Сделать Freestyle Job, который будет запускать `molecule test` из любого вашего репозитория с ролью

#### Я правильно понимаю, что в этом задании нужно сделать скрип, который скачат репозиторий с ролью и запустит команду molecule test  в диреткории с ролью? 

![1 task](https://github.com/ALEMOLOKOV/Jenkins/assets/109212419/c66cab33-08f4-4a14-b63d-edffe9e9cef8)

  
2. Сделать Declarative Pipeline Job, который будет запускать `molecule test` из любого вашего репозитория с ролью.
3. Перенести Declarative Pipeline в репозиторий в файл `Jenkinsfile`.
4. Создать Multibranch Pipeline на запуск `Jenkinsfile` из репозитория.
5. Создать Scripted Pipeline, наполнить его скриптом из [pipeline](./pipeline).
6. Внести необходимые изменения, чтобы Pipeline запускал `ansible-playbook` без флагов `--check --diff`, если не установлен параметр при запуске джобы (prod_run = True). По умолчанию параметр имеет значение False и запускает прогон с флагами `--check --diff`.
7. Проверить работоспособность, исправить ошибки, исправленный Pipeline вложить в репозиторий в файл `ScriptedJenkinsfile`.
8. Отправить ссылку на репозиторий с ролью и Declarative Pipeline и Scripted Pipeline.
9. Сопроводите процесс настройки скриншотами для каждого пункта задания!!
