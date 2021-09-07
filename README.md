# Flask Docs Translation


## Contributing Guide


### Installation

- Click the "Fork" button to fork this repository on GitHub.
- Clone your fork repository locally (replace `{username}` with your username):

```
$ git clone https://github.com/{username}/flask-docs-fr.git
$ cd flask-docs-fr
$ git remote add upstream https://github.com/vlevieux/flask-docs-fr
```

- Create a virtual environment and install requirements:

For Linux/macOS:

```
$ python3 -m venv env
$ source env/bin/activate
$ python -m pip install --upgrade pip setuptools
$ pip install -r requirements/dev.txt
$ pip install -e .
$ pre-commit install
```

For Windows:

```
> python -m venv env
> env\Scripts\activate
> python -m pip install --upgrade pip setuptools
> pip install -r .\requirements\dev.txt
> pip install -e .
> pre-commit install
```


### Self-Assignment

- Open <https://github.com/vlevieux/flask-docs-fr/edit/main/README.md>.
- Find the "Translation To-do List" section, mark the chapter you want to
translate in following format:

```
- [ ] example @your_username Your Name
```

You can link the username to your GitHub profile:

```
- [ ] example [@your_username](https://github.com/your_username) Your Name
```

- Leave a commit message (e.g., "Assign example to @your_username"), then click the
"Propose changes" button to create a PR.

### Recommended Translation software

As explained below, translations are done using .po files. One good editor is
[POEdit](https://poedit.net/) (not to be confused with POEditor)

### Translation

- When the self-assignment PR is merged, create a new branch locally
(be sure to update the example branch name, for example, `translate-cli`):

```
$ git fetch upstream
$ git checkout -b your-branch-name upstream/main
```

- Translate the `.po` file in the `docs/locales/fr/LC_MESSAGES` directory.

An example of one such file, from docs/.../index.po, is given below.

```po
#: ../../index.rst:4
msgid "Welcome to Flask"
msgstr "Bienvenue sur Flask"
```

Another case, msgid is multi-line text and contains reStructuredText syntax:

```po
#: ../../index.rst:11
msgid ""
"Welcome to Flask's documentation. Get started with :doc:`installation` "
"and then get an overview with the :doc:`quickstart`."
msgstr ""
"Bienvenue sur la documentation de Flask. Commencez par consulter le document "
":doc:`installation`, puis obtenez un aperçu avec le document :doc:`quickstart`."
```

Please be careful not to break reST notation. Most
[po-editors](https://www.gnu.org/software/trans-coord/manual/web-trans/html_node/PO-Editors.html) will help you with that.

- Mark the chapter as finished (fill the checkbox with "x"):

```
- [x] example @your_username Your Name
```

- Update the `Last-Translator` field at the top of the `.po` file.
- Commit the changes:

```
$ git add docs/locales/fr/LC_MESSAGES/example.po README.md
$ git commit -m "Translate docs/example"
```

- Build the docs and preview the changes:

For Linux/macOS:

```
$ cd docs
$ make html
```

For Windows:

```
> cd docs
> .\make.bat html
```

Open `{project_location}/docs/_build/html/index.html` in your browser to view the docs.

- If everything is working as expected, push the changes to GitHub:

```
$ git push origin your-branch-name
```

- Open the home page of your forked repository, you will see a notice about
the new branch. Click the "Compare & pull request" button to create a PR.
- The translation coordinator will review your PR very soon. Thank you!


## Translation To-do List

Be sure only mark one chapter at a time, mark another one when the former
PR is created. Unless it's a long chapter, we may reset the assignment
if you doesn't finish the translation in ten days.


### docs/

- [x] advanced_foreword (reserved) @vlevieux Victor LEVIEUX
- [ ] appcontext
- [ ] async-await
- [ ] becomingbig
- [ ] blueprints
- [ ] changes
- [ ] cli
- [ ] config
- [ ] contributing
- [ ] debugging
- [ ] design
- [x] errorhandling @vlevieux Victor LEVIEUX
- [ ] extensiondev
- [ ] extensions
- [x] foreword (reserved) @vlevieux Victor LEVIEUX
- [ ] htmlfaq
- [x] index (reserved) @vlevieux Victor LEVIEUX
- [x] installation (reserved) @vlevieux Victor LEVIEUX
- [x] logging (reserved) @Mindiell
- [x] quickstart (reserved)  @vlevieux Victor LEVIEUX
- [ ] reqcontext
- [ ] security
- [ ] server
- [ ] shell
- [ ] signals
- [x] templating @vlevieux Victor LEVIEUX
- [x] testing @vlevieux Victor LEVIEUX
- [ ] views


### docs/tutorial/ (reserved)

- [x] blog @vlevieux Victor LEVIEUX
- [x] database @vlevieux Victor LEVIEUX
- [x] deploy @vlevieux Victor LEVIEUX
- [x] factory @vlevieux Victor LEVIEUX
- [x] index @vlevieux Victor LEVIEUX
- [x] install @vlevieux Victor LEVIEUX
- [x] layout @vlevieux Victor LEVIEUX
- [x] next @vlevieux Victor LEVIEUX
- [x] static @vlevieux Victor LEVIEUX
- [x] templates @vlevieux Victor LEVIEUX
- [x] tests @vlevieux Victor LEVIEUX
- [x] views @vlevieux Victor LEVIEUX


### docs/deploying/

- [x] asgi (reserved) @Mindiell
- [x] cgi (reserved) @Mindiell
- [x] fastcgi (reserved) @Mindiell
- [x] index (reserved) @Mindiell
- [x] mod_wsgi (reserved) @Mindiell
- [x] uwsgi (reserved) @Mindiell
- [x] wsgi-standalone (reserved) @Mindiell


### docs/patterns/

- [ ] appdispatch
- [ ] appfactories
- [ ] caching
- [ ] celery
- [ ] deferredcallbacks
- [ ] distribute
- [ ] fabric
- [ ] favicon
- [ ] fileuploads
- [ ] flashing
- [ ] index
- [ ] jquery
- [ ] lazyloading
- [ ] methodoverrides
- [ ] mongoengine
- [ ] packages
- [ ] requestchecksum
- [ ] singlepageapplications
- [ ] sqlalchemy
- [ ] sqlite3
- [ ] streaming
- [ ] subclassing
- [ ] templateinheritance
- [ ] urlprocessors
- [ ] viewdecorators
- [ ] wtforms


## docs/api

- [ ] L0~L1000
- [ ] L1000~L1500
- [ ] L1500~L2000
- [ ] L2000~L2500
- [ ] L2500~L3000
- [ ] L3000~L3500
- [ ] L3500~L4000
- [ ] L4000~L4500
- [ ] L4500~L5000
- [ ] L5000~L5500
- [ ] L5500~L6000
- [ ] L6000~L6500
