Gist: The Script
================

Works great with Gist: The Website.

Installation
------------
rubygems preparation
```bash
$ sudo apt-get install ruby
$ sudo apt-get install rubygems
$ sudo apt-get install libopenssl-ruby
```

clone this repo's spec and install
```bash
$ git clone git://github.com/watanabe0621/gist.git
$ pushd gist
$ gem build gist.gemspec
$ sudo gem install ./gist-3.1.0.gem
$ sudo ln -s /var/lib/gems/1.8/gems/gist-3.1.0/bin/gist /usr/local/bin
$ popd
```

add "require 'rubygems'" on a "require 'gist'"  
This problem is just fixing.

Authentication
--------------
```bash
$ git config --global gist.url "github enterprize url"
$ gist -l
```

Use
---

```bash
$ gist < file.txt
$ echo secret | gist --private # or -p
$ echo "puts :hi" | gist -t rb
$ gist script.py
$ gist script.js notes.txt
$ pbpaste | gist -p # Copy from clipboard - OSX Only
$ gist -
the quick brown fox jumps over the lazy dog
```

Defaults
--------

You can set a few options in your git config (using git-config(1)) to
control the default behavior of gist(1).

* gist.private - boolean (yes or no) - Determines whether to make a gist
  private by default

* gist.extension - string - Default extension for gists you create.

* gist.browse - boolean (yes or no) - Whether to open the gist in your
  browser after creation. Default: yes

Proxies
-------

Set the HTTP_PROXY env variable to use a proxy.

```bash
$ HTTP_PROXY=host:port gist file.rb
```

Manual
------

Visit <http://defunkt.github.com/gist/> or use:

```bash
$ gist -m
```

Bugs
----

<https://github.com/defunkt/gist/issues>
