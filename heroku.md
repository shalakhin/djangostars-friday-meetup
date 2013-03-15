# Heroku
## Deploy it, Luke!

[Install toolbelt](https://toolbelt.heroku.com/)

---
= data-x="1000"

# Workflow

* Develop applications as you did it before (I hope you used git)
* `heroku create`
* `git push heroku master`
* PROFIT!!!

---
= data-x="1000"


# How it works

* [How heroku works](http://www.heroku.com/how)
* [How they work](https://addons.heroku.com/provider/resources/technical/how/overview)

---
= data-x="1000"

# Procfile and runtime.txt

Procfile example:

	web: cd src/ && gunicorn livres.wsgi:application -b 0.0.0.0:$PORT -w 4

---
= data-x="1000"


# CLI - part 1

`heroku`:

    login
    create
    config:add
    addons:add
    logs --tail
    ps:scale web=2
    run
    apps:rename

# CLI - part 2

https://devcenter.heroku.com/articles/custom-domains#dns-setup

    heroku domains:add livres.djangostars.com

livres.djangostars.com should be a CNAME recored for heroku original domain

Static and media files handling 

    django-storages http://django-storages.readthedocs.org/en/latest/

    kensa create

---
= data-x="1000"

# Buildpacks and PaaS

* [GeoDjango](https://github.com/cirlabs/heroku-buildpack-geodjango)
* [Go](https://github.com/kr/heroku-buildpack-go)
* [Python 3](https://github.com/heroku/heroku-buildpack-python/pull/64)

---
= data-x="1000"

# Add-ons

[Addons link](https://addons.heroku.com/)
![addons](https://www.evernote.com/shard/s46/sh/5613f48c-173b-4757-b954-ed657a4d5700/e801bc26946f6cf330fc332c2e990f2f/res/e5380e15-d380-42f9-91b9-2ace041c19bc/skitch.png?resizeSmall&width=832)

---
= data-x="1000"

# Free add-ons

    $ heroku addons:add cloudamqp:lemur
    $ heroku-postgresql:dev
    $ scheduler:standard
    $ memcache:5mb
    $ newrelic:standard
    $ pgbackups:auto-month
    $ sentry:developer


---
= data-x="1000"

# My Skeleton O_o

[My skeleton](https://github.com/OShalakhin/django-skeleton)

---
= data-x="1000"

# Heroku django-skel

[RTD](http://django-skel.readthedocs.org/en/latest/)

---
= data-x="1000"

# Deploy Django project

    git clone https://github.com/rootart/livres-backend
    heroku create
    heroku addons:add heroku-postgresql:dev
    heroku config:add DJANGO_SETTINGS_MODULE="livres.settings"
    heroku run python src/manage.py syncdb --all
    git push heroku master


Afterwords:


    heroku run python manage.py syncdb --all

---
= data-x="1000"

# Yet another Django-thing

in `settings.py`

    import dj_database_url
    DATABASES['default'] = dj_database_url.config()

---
= data-x="1000"


# Deploy Golang project

    echo 'web: simple' > Procfile
    echo 'simple' > .godir
    heroku create -b https://github.com/kr/heroku-buildpack-go.git
    git push heroku master

---
= data-x="1000"

# Alternatives

* Ep.io
* Gondor
* dotCloud

---
= data-x="1000"

# Costs

---
= data-x="1000"

# Literature

* [Build your own addon](https://addons.heroku.com/provider/resources/technical/build/overview)
* 
