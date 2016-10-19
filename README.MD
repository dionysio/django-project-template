# Django 1.10+ project template

This is a simple Django 1.10+ project template with my preferred setup. I wanted to make the least amount of assumptions to make this as generic as possible. To run it you need Django 1.10 and [django-debug-toolbar](https://django-debug-toolbar.readthedocs.org) for dev environment. 


## Features

- Django 1.10
- jQuery 3.1.1, Bootstrap 3.3.7, Font Awesome 4.6.3 included
- [the base template](base/templates/base.html) and all the other templates are bootstrap-based
- configuration is split:
    * secret - stuff that should not be in public repo (or atleast encrypted) like credentials, secret keys, that kind of stuff
    * settings - common base settings which should be for production
    * local - overwritten settings with development settings - maybe different db, MEDIA_ROOT etc
- Custom templates for 403, 404, 500 errors with i18n support
- Get value insight and debug information while on `local` with [django-debug-toolbar](https://django-debug-toolbar.readthedocs.org).
- _manage.py for `local`, manage.py for `production`


## How to install

```bash
$ django-admin.py startproject project_name
  --template=https://github.com/dionysio/django-project-template/archive/master.zip \
$ pip install -r requirements.txt
$ python _manage.py migrate
$ python _manage.py runserver
```

## Possible improvements

- more customization to the production settings - stuff like SSL, template cached loader...
- maybe rework the settings code a bit and split it differently?
- navbar might need some work, especially the navbar-collapse

## License

MIT License

Copyright (c) 2016 Dionyz Lazar

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.