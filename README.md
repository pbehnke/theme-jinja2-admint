# [Jinja2 Theme - AdminT (Free Version)](https://theme-jinja2-admint.appseed.us/)

> Template Theme provided by [AppSeed](https://appseed.us) - Features:

- UI Kit: **AdminT Dashboard** (Free Version) by **YooKits**
- Render Engine: Flask / [Jinja2](https://jinja.palletsprojects.com/)
- **[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)** (preserve the footer credit to YooKits)
- Free support via **Github** issues tracker
- Paid 24/7 Live Support via [Discord](https://discord.gg/fZC6hup).

> Links

- [Jinja2 Theme - AdminT (Free Version)](https://theme-jinja2-admint.appseed.us/) - LIVE Demo

<br />

## UI Kit - [AdminT (Free Version)](https://yookits.com/product/admint-bootstrap-admin-template/?ref=appseed)

*Vendor Notes* - **[AdminT](https://yookits.com/product/admint-bootstrap-admin-template/?ref=appseed)** is the swiss army knife of the dashboard templates. 
You can create applications of any kind with it. We carefully crafted every component based on a cohesive design system. Your app will look pro with Admint magic. It’s completely free & open-source. Grab it today and build beautiful apps.

> Links

- [AdminT (Free Version)](https://yookits.com/product/admint-bootstrap-admin-template/?ref=appseed) - product page
- [AdminT](https://github.com/yookits/admint/) - Html version source code (Github)

<br />

![Jinja2 Theme - AdminT (Free Version) - Template project provided by AppSeed.](https://raw.githubusercontent.com/app-generator/theme-jinja2-admint/master/media/theme-jinja2-admint-screen.png)

<br />

## Build from sources

```bash
$ # Clone the sources
$ git clone https://github.com/app-generator/theme-jinja2-admint.git
$ cd theme-jinja2-admint
$
$ # Virtualenv modules installation (Unix based systems)
$ virtualenv env
$ source env/bin/activate
$
$ # Virtualenv modules installation (Windows based systems)
$ # virtualenv env
$ # .\env\Scripts\activate
$
$ # Install requirements
$ pip3 install -r requirements.txt
$
$ # Set the FLASK_APP environment variable
$ (Unix/Mac) export FLASK_APP=run.py
$ (Windows) set FLASK_APP=run.py
$ (Powershell) $env:FLASK_APP = ".\run.py"
$
$ # Set up the DEBUG environment
$ # (Unix/Mac) export FLASK_ENV=development
$ # (Windows) set FLASK_ENV=development
$ # (Powershell) $env:FLASK_ENV = "development"
$
$ # Run the Jinja Template
$ # --host=0.0.0.0 - expose the app on all network interfaces (default 127.0.0.1)
$ # --port=5000    - specify the app port (default 5000)  
$ flask run --host=0.0.0.0 --port=5000
$
$ # Access the UI in browser: http://127.0.0.1:5000/
```

<br />

## Code-base structure

The project has a simple structure, represented as bellow:

```bash
< PROJECT ROOT >
   |
   |-- app/__init__.py
   |-- app/
   |    |-- static/
   |    |    |-- <css, JS, images>         # CSS files, Javascripts files
   |    |
   |    |-- templates/
   |    |    |
   |    |    |-- includes/                 # Page chunks, components
   |    |    |    |
   |    |    |    |-- navigation.html      # Top bar
   |    |    |    |-- sidebar.html         # Left sidebar
   |    |    |    |-- scripts.html         # JS scripts common to all pages
   |    |    |    |-- footer.html          # The common footer
   |    |    |
   |    |    |-- layouts/                  # App Layouts (the master pages)
   |    |    |    |
   |    |    |    |-- base.html            # Used by common pages like index, UI
   |    |    |    |-- base-fullscreen.html # Used by auth pages (login, register)
   |    |    |
   |    |  index.html                      # The default page
   |    |  login.html                      # Auth Login Page
   |    |  register.html                   # Auth Registration Page
   |    |  page-404.html                   # Error 404 page (page not found)
   |    |  page-500.html                   # Error 500 page (server error)
   |    |    *.html                        # All other pages provided by the UI Kit
   |
   |-- requirements.txt
   |
   |-- run.py
   |
   |-- ************************************************************************
```

<br />

## Deployment

The project comes with a basic configuration for [Docker](https://www.docker.com/), [Gunicorn](https://gunicorn.org/), and [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/).

<br />

### [Docker](https://www.docker.com/) execution
---

The steps to start the template using Docker:

> Get the code

```bash
$ git clone https://github.com/app-generator/theme-jinja2-admint.git
$ cd theme-jinja2-admint
```

> Start the app in Docker

```bash
$ sudo docker-compose pull && sudo docker-compose build && sudo docker-compose up -d
```

Visit `http://localhost:5005` in your browser. The app should be up & running.

<br />

### [Gunicorn](https://gunicorn.org/)
---

Gunicorn 'Green Unicorn' is a Python WSGI HTTP Server for UNIX.

> Install using pip

```bash
$ pip install gunicorn
```
> Start the app using gunicorn binary

```bash
$ gunicorn --bind 0.0.0.0:8001 run:app
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.

<br />

### [Waitress](https://docs.pylonsproject.org/projects/waitress/en/stable/)
---

Waitress (Gunicorn equivalent for Windows) is meant to be a production-quality pure-Python WSGI server with very acceptable performance. It has no dependencies except ones that live in the Python standard library.

> Install using pip

```bash
$ pip install waitress
```
> Start the app using [waitress-serve](https://docs.pylonsproject.org/projects/waitress/en/stable/runner.html)

```bash
$ waitress-serve --port=8001 run:app
Serving on http://localhost:8001
```

Visit `http://localhost:8001` in your browser. The app should be up & running.

<br />

## Credits & Links

- [Flask Framework](https://www.palletsprojects.com/p/flask/) - The official website

<br />

---
[Jinja2 Theme - AdminT (Free Version)](https://theme-jinja2-admint.appseed.us/) - Provided by **AppSeed** [Web App Generator](https://appseed.us/app-generator).
