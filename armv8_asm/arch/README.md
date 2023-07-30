SSH server application

#docker version
- Docker version 24.0.2, build cb74dfc

#set-up list

- latest arch version
- pacman
- open-ssh
- vi
- arm-none-eabi-gcc
- binutils
- appuser and root account
- set port 22
- set editable directory
- start SSH

# build command
docker build -t armv8asmapp .

# run command
docker run -d -p 2222:22 -v ".":/app  --name armv8asmapp1 armv8asmapp

# ssh access
ssh -p 2222 root@localhost


cat /etc/os-release 

NAME="Arch Linux"
PRETTY_NAME="Arch Linux"
ID=arch
BUILD_ID=rolling
VERSION_ID=20230723.0.166908
ANSI_COLOR="38;2;23;147;209"
HOME_URL="https://archlinux.org/"
DOCUMENTATION_URL="https://wiki.archlinux.org/"
SUPPORT_URL="https://bbs.archlinux.org/"
BUG_REPORT_URL="https://bugs.archlinux.org/"
PRIVACY_POLICY_URL="https://terms.archlinux.org/docs/privacy-policy/"
LOGO=archlinux-logo


uname -r
	5.15.49-linuxkit-pr
uname -a
	Linux 1fc93f8f3e26 5.15.49-linuxkit-pr #1 SMP Thu May 25 07:17:40 UTC 2023 x86_64 GNU/Linux
