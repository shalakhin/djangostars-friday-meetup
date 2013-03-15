# Heroku
## Deploy it, Luke!

---
= data-x="1000"

# Step 0. Deploy


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

# Workflow

---
= data-x="1000"



# How it works

---
= data-x="1000"

# Procfile and runtime.txt

	web: cd src/ && gunicorn livres.wsgi:application -b 0.0.0.0:$PORT -w 4

---
= data-x="1000"


# CLI

---
= data-x="1000"


# Auth

---
= data-x="1000"

# Buildpacks and PaaS

* GeoDjango (tell about PostGIS and Heroku)
* Go
* Python 3

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

# Deploy Golang project

---
= data-x="1000"

# Alternatives

Ep.io
Gondor
dotCloud

---
= data-x="1000"

# Costs

---
= data-x="1000"

# Literature
