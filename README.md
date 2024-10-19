# Ansible Role - storage-init

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

## Examples

Example to create a 1 TB storage block that will eventually be assigned to `/dev/sdb1/`

```yaml
- hosts: all
  remote_user: root

  vars_files:
    - ./vars/configs/{{ inventory_hostname }}.yml

  vars:
    # Better to have in common vars_files input file
    mnt_dir: "/mnt/data"
    partition_type: xfs
    device_name: sdb
    partition_num: 1

  roles:
    - { role: nholuong.storage-init }
```

## Linting

```bash
yamllint -c yamllint.yaml .
ansible-lint .
```

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟