# ДЗ 01 = manual_kernel_update

Изменениря от [оригинального](manual/manual.md) сценария:
1. Новая версия оригинального образа с yandex 
2. Исправленая часть provisining-a, где вносятся изменения в `/etc/sudoers.d/vagrant`, иначе была ошибка на этапе запуска скриптов

Запуск packer

```
packer> packer build centos-7-9.json
...
==> Wait completed after 8 minutes 36 seconds

==> Builds finished. The artifacts of successful builds are:
--> centos-7.9: 'virtualbox' provider box: centos-7.9.2009-kernel-5-x86_64-Minimal.box
```

Публикуем в Vagrant Cloud образ

Проверяем:

```
> vagrant up
...
> vagrant ssh
Last login: Mon Nov 16 06:08:54 2020 from gateway
[vagrant@localhost ~]$ uname -r
5.9.8-1.el7.elrepo.x86_64
```




