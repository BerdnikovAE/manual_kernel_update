# �� 01 = manual_kernel_update

���������� �� [�������������](manual/manual.md) ��������:
1. ����� ������ ������������� ������ � yandex 
2. ����������� ����� provisining-a, ��� �������� ��������� � `/etc/sudoers.d/vagrant`, ����� ���� ������ �� ����� ������� ��������

������ packer

```
01\packer> packer build centos-7-9.json
...
==> Wait completed after 8 minutes 36 seconds

==> Builds finished. The artifacts of successful builds are:
--> centos-7.9: 'virtualbox' provider box: centos-7.9.2009-kernel-5-x86_64-Minimal.box
```

��������� � Vagrant Cloud �����

���������:

```

01\test> vagrant init berdnikovae/centos-7-9
01\test> vagrant up
...
01\test> vagrant ssh
Last login: Mon Nov 16 06:08:54 2020 from gateway
[vagrant@localhost ~]$ uname -r
5.9.8-1.el7.elrepo.x86_64
```




