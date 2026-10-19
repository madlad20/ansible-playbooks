# ansible-playbooks

SKPVA kursuse Ansible labid – Chris-Luca Homenja (ITS24)

## Keskkond

| Masin | Roll | OS | IP |
|---|---|---|---|
| homenjaansible | Ansible-server | Debian 13 | 192.168.33.130 |
| homenjaweb | klient1 | Debian 13 | 192.168.33.131 |
| homenjacentos | klient2 | CentOS Stream 10 | 192.168.46.41 |

## Failid

- `hosts` – inventory (Lab 1), serveris `/root/hosts`
- `ansible.cfg` – Ansible seadistus (Lab 1), serveris `/root/.ansible.cfg`
- `apache2.yml` – Lab 2: Apache2 paigaldus, userdir moodul ja kasutaja `user` koduleht (`http://klient1/~user/`)
- `index.yml` – Lab 2 iseseisev ülesanne: igale kliendile unikaalne avaleht hostinime ja IP-ga

## Käivitamine

```
ansible -m ping all
ansible-playbook --check /root/playbooks/apache2.yml
ansible-playbook /root/playbooks/apache2.yml
ansible-playbook /root/playbooks/index.yml
```
