SSH server application

#docker version
- Docker version 24.0.2, build cb74dfc

#set-up list

- latest ubuntu version
- apt-get
- open-ssh
- vim
- root account
- set port 22
- set editable directory
- start SSH

# build command
docker build -t sshapp .

# run command
docker run -d -p 2222:22 -v ".":/app sshapp --name sshapp1 sshapp

# ssh access
ssh -p 2222 root@localhost


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

uname -r
5.15.49-linuxkit-pr

uname -a
Linux 45b4abfd5895 5.15.49-linuxkit-pr #1 SMP Thu May 25 07:17:40 UTC 2023 x86_64 x86_64 x86_64 GNU/Linux