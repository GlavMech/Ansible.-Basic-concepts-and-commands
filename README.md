# Ansible.-Basic-concepts-and-commands


# Отчет по развертыванию WordPress на Debian 12 через Ansible

1. Создал виртуальную машину Debian 12 с помощью Vagrant:
   - Запустил 
   ```python
      vagrant up
   ```
   - Узнал IP машины через ```python vagrant ssh-config ``` → 192.168.56.10

2. Настроил Ansible inventory файл `/path/to/inventory.yaml`:
   - all:
   - hosts:
   - debian:
   - ansible_host: 192.168.56.10
   - ansible_user: vagrant

3. Подготовил playbook `wordpress-playbook.yaml` с установкой Apache, MariaDB, PHP и WordPress.

4. Запустил playbook командой:
  ```python
  ansible-playbook -i inventory.yaml wordpress-playbook.yaml
  ```
5. Сохранил лог выполнения в файл `playbook_output.log` (файл прилагаю).

6. Проверил в браузере по адресу http://192.168.56.10 — успешно загрузилась страница WordPress.

---

Файлы, переданные на проверку:

- `wordpress-playbook.yaml`
- `inventory.yaml`
- `playbook_output.log`
