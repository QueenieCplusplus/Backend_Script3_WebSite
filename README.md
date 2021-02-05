# Backend_Script3_WebSite
Django using python 3.8 &amp; pip3 &amp; Virtualenv


![](Django using python 3.8 &amp; pip3 &amp; Virtualenhttps://github.com/QueenieCplusplus/Backend_Script3_WebSite/raw/main/fake_site.png)


* Virtualenv

備註 爬蟲僅需要 python2 然而網站建議用 python 3 ，前者為全域，後者建議用虛擬機。


* Env Path

      $ which python3 = path

      $ virtualen -p  path  proj_name

      KatesAndroiddeMacBook-Pro:~ katesandroid$ source proj_name/bin/activate
      (proj_name) KatesAndroiddeMacBook-Pro:~ katesandroid$ 


      (pron_name): $ pip list


example:

      (katesP) KatesAndroiddeMacBook-Pro:~ katesandroid$ pip list
      Package    Version
      ---------- -------
      pip        21.0.1
      setuptools 52.0.0
      wheel      0.36.2


* Leave

      (katesP) KatesAndroiddeMacBook-Pro:~ katesandroid$ deactivate


* Installation 

   then install Django 3.1.6 =>

      (katesP) KatesAndroiddeMacBook-Pro:~ katesandroid$ pip3 install django

            Collecting django
              Downloading Django-3.1.6-py3-none-any.whl (7.8 MB)
                 |████████████████████████████████| 7.8 MB 7.1 MB/s 
            Collecting pytz
              Downloading pytz-2021.1-py2.py3-none-any.whl (510 kB)
                 |████████████████████████████████| 510 kB 4.6 MB/s 
            Collecting asgiref<4,>=3.2.10
              Downloading asgiref-3.3.1-py3-none-any.whl (19 kB)
            Collecting sqlparse>=0.2.2
              Downloading sqlparse-0.4.1-py3-none-any.whl (42 kB)
                 |████████████████████████████████| 42 kB 1.6 MB/s 
            Installing collected packages: sqlparse, pytz, asgiref, django

            Successfully installed asgiref-3.3.1 django-3.1.6 pytz-2021.1 sqlparse-0.4.1


* check version => 

          python3 -m django —version

* to do a fake website's dir =>

         mkdir test-django
* cd to it

* do a fake website

      django-admin startproject site_name

* cd to site_name

* run server using manage.py

            python3 manage.py runserver (命令)
            //即從此文件夾內運行網站服務器

* 缺文件補上文件:

      ^C(katesP) KatesAndroiddeMacBook-Pro:fakeSite katesandroid$ python3 manage.py migrate
      Unknown command: 'migigrate'. Did you mean migrate?
      Type 'manage.py help' for usage.
      (katesP) KatesAndroiddeMacBook-Pro:fakeSite katesandroid$ python3 manage.py migrate
      Operations to perform:
        Apply all migrations: admin, auth, contenttypes, sessions


                      Operations to perform:
                        Apply all migrations: admin, auth, contenttypes, sessions
                      Running migrations:
                        Applying contenttypes.0001_initial... OK
                        Applying auth.0001_initial... OK
                        Applying admin.0001_initial... OK
                        Applying admin.0002_logentry_remove_auto_add... OK
                        Applying admin.0003_logentry_add_action_flag_choices... OK
                        Applying contenttypes.0002_remove_content_type_name... OK
                        Applying auth.0002_alter_permission_name_max_length... OK
                        Applying auth.0003_alter_user_email_max_length... OK
                        Applying auth.0004_alter_user_username_opts... OK
                        Applying auth.0005_alter_user_last_login_null... OK
                        Applying auth.0006_require_contenttypes_0002... OK
                        Applying auth.0007_alter_validators_add_error_messages... OK
                        Applying auth.0008_alter_user_username_max_length... OK
                        Applying auth.0009_alter_user_last_name_max_length... OK
                        Applying auth.0010_alter_group_name_max_length... OK
                        Applying auth.0011_update_proxy_permissions... OK
                        Applying auth.0012_alter_user_first_name_max_length... OK
                        Applying sessions.0001_initial... OK
* 補完文件後再次運行：


      $ python3 manage.py runserver
      Watching for file changes with StatReloader
      Performing system checks...

* 本機上運行成功：

        System check identified no issues (0 silenced).
        February 05, 2021 - 06:27:08
        Django version 3.1.6, using settings 'fakeSite.settings'
        Starting development server at http://localhost:8000/
        Quit the server with CONTROL-C.

* 網站的相關文件


          proj_name/site_name/    db.sqlite3	  fakeSite	    manage.py


