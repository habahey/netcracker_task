# netcracker_task

# Playbook для развернутх VM 
 centos 8:     hostname c8.local
 ubuntu 21.04: hastname u21.local  

# Задача:
Единый ansible playbook для c8.local и u21.local
c8.local должен быть в группе frontend
u21.local должен быть в группе backend
 - для ОС centos playbook должен применять следующие изменения
 * selinux: disable
 * firewalld: disable
 - для группы frontend playbook должен установить и сконфигурировать nginx
 - конфигурация nginx должна делать проксирование с порта 80 на порт 19999 в группу backend
 - для группы backend playbook должен установить из официальных репозиториев приложение netdata и запустить его на порту 19999
