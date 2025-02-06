# ansible-test-role

## Быстрый старт

1\. Устанавливаем зависимости
```shell
ansible-galaxy install -r requirements.yaml
```

2\. Подготавливаем [инвентори-файл](./inventories/inventory.yaml).

3\. Запускаем роль указывая через флаг **-t** один, несколько или все теги (через запятую): encryption, cpu_perf, network, cpu_info.
```shell
ansible-playbook -i inventories/inventory.yaml -t <теги> encryption prepare-vm.yaml
```
