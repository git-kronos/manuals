## postgres in ubuntu

**postgresql**

    sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'

    wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -

    sudo apt-get update

    sudo apt-get -y install postgresql

    sudo passwd postgres

    su postgres

    psql -c "ALTER USER postgres PASSWORD 'password';"

**pgadmin**

    sudo curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add

    sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'

    sudo apt install pgadmin4
