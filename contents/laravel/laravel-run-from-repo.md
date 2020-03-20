# Steps to run a Laravel App from a repository *(Ubuntu tutorial)*

***

## 1. Clone the repo

    git clone the_project_path your_project_name


## 2. Cd into the project

    cd your_project_name


## 3. Set the permissions

*From: https://askubuntu.com/a/46371/1036442*

> Add your user to the group www-data:

    sudo gpasswd -a "$USER" www-data


> Set the permissions to the group www-data:

    sudo chown -R "$USER":www-data /var/www/html
    find /var/www/html -type f -exec chmod 0660 {} \;
    sudo find /var/www/html -type d -exec chmod 2770 {} \;


> Set other permisions:

    sudo chmod -R 777 /var/www/html/laravel/cms/storage
    sudo chmod -R 777 /var/www/html/laravel/cms/bootstrap/cache/


## 4. Commited the files

Some files will be appear as changed for git in this point. Add all
and commit to save permissions changes:

    git add -all
    git commit -m 'updated file permissions'


## 5. Composer install


## 6. Create the .env file and setting it

If the **.env.example** file exists:

    cp .env.example .env

*If the example file is not available search the correct one of your*
*Laravel version: https://github.com/laravel/laravel/tree/master*


## 7. Generate key

    php artisan key:generate


## 8. Create the DB

Create an empty DB named as the setted in the *.env file* and assign the
correct user and privileges.


## 9. Run the migrations

    php artisan migrate


## 10. Seed the DB if it's neccessary

    php artisan db:seed


***

[Go to index](../../README.md)
