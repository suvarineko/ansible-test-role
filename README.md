# ansible-test-role

## Совместимость
Роль протестирована на версии ansible **core 2.15.8**, но должна также работать на любой версии **core** выше 2.10.

## Быстрый старт
1\. Устанавливаем зависимости
```shell
ansible-galaxy install -r requirements.yaml
```

2\. Подготавливаем [инвентори-файл](./inventories/inventory.yaml). Если необходимо, то в [плейбуке](./prepare-vm.yaml) в параметре **hosts** меняем значение на нужную группу хостов или же указываем все хосты (значение **all**).

3\. Запускаем роль указывая через флаг **-t** один, несколько или все теги (через запятую): encryption, cpu_perf, network, cpu_info.
```shell
ansible-playbook -i inventories/inventory.yaml -t <теги> encryption prepare-vm.yaml
```

## Параметры в инвентори
|Параметр|Значение|
|--------|--------|
|network.rename_to|Новое имя сетевого интерфейса|
|disk.encrypt|Имя диска для шифрования, например - /dev/xvdf|
|disk.encrypt_type|Тип шифрования: luks1 или luks2|

