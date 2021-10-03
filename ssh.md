# SSH config

## **on server:**

* `sudo apt install openssh-server`
* `sudo systemctl status ssh`
* `sudo service ssh status`
* `sudo systemctl enable --now ssh`
* `sudo systemctl status ufw`
* `sudo ufw allow ssh`

## **on client:**

* `ssh-keygen -f test_key`
* `ssh-copy-id -i ~/.ssh/test_server_key user@host`

## **recomended configuration on client side:**

* `authorized_keys`
* `/etc/ssh/sshd_config "# PasswordAuthentication yes" -> "PasswordAuthentication no"`
* `sudo systemctl reload sshd`

## **authorise transfered ssh files:**

>`used ssh key activate in linux`
>
>`chown $(whoami):$(whoami) ~/.ssh/id_rsa*`
>
> `chmod 600 ~/.ssh/id_rsa`
>
> `chmod 644 ~/.ssh/id_rsa.pub`
>
> `chmod 600 ~/.ssh/config`
>
> `chown $USER ~/.ssh/config`
>