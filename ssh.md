
# SSH config
###### on server
- sudo apt install openssh-server (sudo pacman -S openssh)

- sudo systemctl status ssh
- sudo systemctl enable --now ssh

- sudo systemctl status ufw
- sudo ufw allow ssh

###### on client
- ssh-keygen -f test_key
- ssh-copy-id -i ~/.ssh/test_server_key user@host
- authorized_keys

- /etc/ssh/sshd_config "# PasswordAuthentication yes" -> "PasswordAuthentication no"
- sudo systemctl reload sshd
