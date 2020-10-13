# sopo
root@sopo:/home/user/labs/sopo# ansible-playbook -i environments/localhost/inventory playbook.yml -D
/usr/local/lib/python2.7/dist-packages/ansible/parsing/vault/__init__.py:44: CryptographyDeprecationWarning: Python 2 is no longer supported by the Python core team. Support for it is now deprecated in cryptography, and will be removed in a future release.
  from cryptography.exceptions import InvalidSignature

PLAY [all] **********************************************************************************************************************************************************************************************************************************

TASK [Gathering Facts] **********************************************************************************************************************************************************************************************************************
[DEPRECATION WARNING]: Distribution Ubuntu 16.04 on host localhost-1 should use /usr/bin/python3, but is using /usr/bin/python for backward compatibility with prior Ansible releases. A future Ansible release will default to using the
discovered platform python for this host. See https://docs.ansible.com/ansible/2.10/reference_appendices/interpreter_discovery.html for more information. This feature will be removed in version 2.12. Deprecation warnings can be disabled
 by setting deprecation_warnings=False in ansible.cfg.
ok: [localhost-1]

TASK [change-ip : Change ip] ****************************************************************************************************************************************************************************************************************
--- before: /etc/network/interfaces
+++ after: /etc/network/interfaces
@@ -13,6 +13,6 @@

 auto enp0s8
 iface enp0s8 inet static
-address 192.168.56.200
+address 192.168.56.201
 netmask 255.255.255.0


changed: [localhost-1]

PLAY RECAP **********************************************************************************************************************************************************************************************************************************
localhost-1                : ok=2    changed=1    unreachable=0    failed=0    skipped=0    rescued=0    ignored=0
