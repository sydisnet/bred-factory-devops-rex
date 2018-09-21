# BRED Factory DevOps - Rentrée DevOps : retours d'expérience

Les slides sont générés à l'aide de l'outil **AsciiDoctor** et le plugin associé permettant de
générer la présentation au format **reveal.js**.


## Pré-requis

Il convient au préalable d'installer un [Runtime Ruby](https://www.ruby-lang.org/fr/ "Runtime Ruby").

Merci de bien vouloir penser à créer une variable d'environnement `RUBY_HOME` puis de modifier le `PATH`
en ajoutant le chemin `%RUBY_HOME%/bin` sous **Linux** (ou `$RUBY_HOME\bin` sous **Windows**).


### Installer AsciiDoctor

Pour installer AsciiDoctor, lancer la commande `gem` suivante :

    $ gem install asciidoctor

Si vous vous trouvez derrière un proxy d'entreprise, penser à paramétrer les deux variables d'environnements `HTTP_PROXY`
et `http_proxy`.


Si tout se passe bien, la log devrait être proche de celle-ci :

    Successfully installed asciidoctor-1.5.7.1
    Parsing documentation for asciidoctor-1.5.7.1
    Done installing documentation for asciidoctor after 2 seconds
    1 gem installed


### Installer Bundler

Pour installer Bundler, de la même manière, lancer la commande `gem` suivante :

    $ gem install bundler

Si tout se passe, la log devrait être proche de celle-ci :

    Fetching: bundler-1.16.5.gem (100%)
    Successfully installed bundler-1.16.5
    Parsing documentation for bundler-1.16.5
    Installing ri documentation for bundler-1.16.5
    Done installing documentation for bundler after 5 seconds
    1 gem installed


### Installer Asciidoctor-Revealjs

Le fichier `Gemfile` présent à la racine précise la dépendance à installer :

    source 'https://rubygems.org'
    
    gem 'asciidoctor-revealjs' # latest released version


Installer les `gems` dans le projet :

    $ bundle config --local github.https true
    $ bundle --path=.bundle/gems --binstubs=.bundle/.bin


Récupérer la version **3.6.0** de **reveal.js** :

    $ git clone -b 3.3.0 --depth 1 https://github.com/hakimel/reveal.js.git


## Générer les slides au format HTML5 reveal.js

Les slides sont au format **AsciiDoctor** dans le fichier `slides.adoc`. Lancer la commande `bundle` suivante :

    $ bundle exec asciidoctor-revealjs slides.adoc


Un fichier `slides.html` est alors généré. Ouvrir le fichier `slides.html` avec un navigateur.


## Commandes

Appuyer sur `s` pour afficher les notes et `Esc` pour pouvoir accéder rapidement à une slide.


