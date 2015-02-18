Rails ERD - Generate Entity-Relationship Diagrams for Rails applications
========================================================================

[Rails ERD](http://voormedia.github.io/rails-erd/) is a Rails plugin that allows you to easily generate a diagram based on your Active Record models. The diagram gives an overview of how your models are related. Having a diagram that describes your models is perfect documentation for your application.

The second goal of Rails ERD is to provide you with a tool to inspect your application's domain model. If you don't like the default output, it is very easy to use the API to build your own diagrams.

Rails ERD was created specifically for Rails and works on versions 3.0-4.2. It uses Active Record's built-in reflection capabilities to figure out how your models are associated.


Preview
-------

Here's an example entity-relationship diagram that was generated by Rails ERD:

![Entity-Relationship Diagram](http://voormedia.github.io/rails-erd/images/entity-relationship-diagram.png)

Browse the [gallery](http://voormedia.github.io/rails-erd/gallery.html) for more example diagrams.


Requirements
---------------

* Ruby 1.9.3+
* ActiveRecord 3.x

Getting started
---------------

See the [installation instructions](http://voormedia.github.io/rails-erd/install.html) for a complete description of how to install Rails ERD. Here's a summary:

* Install Graphviz 2.22+ ([how?](http://voormedia.github.io/rails-erd/install.html))

* Add <tt>gem "rails-erd"</tt> to your application's Gemfile

* Run <tt>bundle exec erd</tt>

### Configuration

Rails ERD has the ability to be configured via the command line or through the use of a YAML file with configuration options set. It will look for this file first at `~/.erdconfig` and then `./.erdconfig` (which will override any settings in `~/.erdconfig`). The format of the file is as follows (shown here with the default settings used if no `.erdconfig` is found):

```
attributes:
  - content
  - foreign_key
  - inheritance
disconnected: true
filename: erd
filetype: pdf
indirect: true
inheritance: false
markup: true
notation: simple
orientation: horizontal
polymorphism: false
sort: true
warn: true
title: sample title
exclude: null
only: null
```


Learn more
----------

More information can be found on [Rails ERD's project homepage](http://voormedia.github.io/rails-erd/).

If you wish to extend or customise Rails ERD, take a look at the [API documentation](http://rubydoc.info/github/voormedia/rails-erd/frames).


About Rails ERD
---------------

Rails ERD was created by Rolf Timmermans (r.timmermans *at* voormedia.com)

Copyright 2010-2015 Voormedia - [www.voormedia.com](http://www.voormedia.com/)


License
-------

Rails ERD is released under the MIT license.
