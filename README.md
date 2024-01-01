# Set up my local environment

## Prerequisites

- Supported OS

```bash
cat /etc/os-release
PRETTY_NAME="Ubuntu 22.04.2 LTS"
NAME="Ubuntu"
VERSION_ID="22.04"
VERSION="22.04.2 LTS (Jammy Jellyfish)"
VERSION_CODENAME=jammy
ID=ubuntu
ID_LIKE=debian
HOME_URL="https://www.ubuntu.com/"
SUPPORT_URL="https://help.ubuntu.com/"
BUG_REPORT_URL="https://bugs.launchpad.net/ubuntu/"
PRIVACY_POLICY_URL="https://www.ubuntu.com/legal/terms-and-policies/privacy-policy"
UBUNTU_CODENAME=jammy
```

- Tools

```bash
sudo apt update

# pip
sudo apt install python3-pip

python3 -m pip -V
pip 22.0.2

# Ansible
python3 -m pip install --user ansible

~/.local/bin/ansible --version
ansible [core 2.16.2]
```

# Usage

- My inventory file is `./hosts`. In this file, an inventory `local` is defined.

```bash
ansible-playbook -i local site.yml
```

## References

- [Ansible Best Practices](https://docs.ansible.com/ansible/2.8/user_guide/playbooks_best_practices.html)
  - Regarding directory structure, I refers [Directory Layout](https://docs.ansible.com/ansible/2.8/user_guide/playbooks_best_practices.html#directory-layout)
