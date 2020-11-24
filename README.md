# sopo
root@sopo:/home/user/labs# docker run --volume /home/user/.ssh:/root/.ssh --volume /home/user/labs/sopo:/sopo --volume /root/.ansible/roles:/root/.ansible/roles/ ansible ansible-playbook -i /sopo/environments/dev/inventory /sopo/playbook.yml -D
/usr/local/lib/python2.7/dist-packages/ansible/parsing/vault/__init__.py:44: CryptographyDeprecationWarning: Python 2 is no longer supported by the Python core team. Support for it is now deprecated in cryptography, and will be removed in a future release.
  from cryptography.exceptions import InvalidSignature
[WARNING]: Found both group and host with same name: dev

PLAY [all] *********************************************************************

TASK [Gathering Facts] *********************************************************
ok: [dev]
[DEPRECATION WARNING]: Distribution Ubuntu 16.04 on host dev should use
/usr/bin/python3, but is using /usr/bin/python for backward compatibility with
prior Ansible releases. A future Ansible release will default to using the
discovered platform python for this host. See https://docs.ansible.com/ansible/
2.9/reference_appendices/interpreter_discovery.html for more information. This
feature will be removed in version 2.12. Deprecation warnings can be disabled
by setting deprecation_warnings=False in ansible.cfg.

TASK [change-ip : Change ip] ***************************************************
--- before: /etc/network/interfaces
+++ after: /etc/network/interfaces
@@ -13,6 +13,6 @@

 auto enp0s8
 iface enp0s8 inet static
-address 192.168.56.202
+address 192.168.56.203
 netmask 255.255.255.0


changed: [dev]

PLAY RECAP *********************************************************************
dev                        : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0

