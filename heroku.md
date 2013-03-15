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
