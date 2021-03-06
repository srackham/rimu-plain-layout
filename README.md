# Rimu Markup Plain Layout

A minimal unstyled HTML5 layout for the _Rimu Markup_
[rimuc](http://rimumarkup.org/reference.html#rimuc-command) command.

This package is also serves as a template for creating new layouts.

## Installation
1. If you haven't already done so install Rimu:

        sudo npm install -g rimu

2. Install this package:

        sudo npm install -g rimu-plain-layout


## Usage
Once this package has been installed then you can use the `rimuc`
command `--layout plain` option to create unstyled HTML5 documents
from Rimu markup. The following example generates an HTML5 file
named `mydocument.html`:

    rimuc --layout plain mydocument.rmu


## How it works
When `--layout <layout-name>` option is specified `rimuc` searches for
a built-in layout with the same name. If it's not found then `rimuc`
attempts to import a nodejs module named `rimu-<layout-name>-layout`
(in this case `rimu-plain-layout`). The imported module contains two
attributes, `header` and `footer`, which return the Rimu header markup
and footer markup respectively.


## Creating new layouts
Creating a new layout is straightforward:

1. Clone the `rimu-plain-layout` [Github
   project](https://github.com/srackham/rimu-plain-layout.git).
2. Replace or edit `header.rmu` and `footer.rmu` files.
3. Edit `package.json` and `README.md` to reflect the new layout name,
   Github repository, author etc.

For more complex header and footer examples take a look at the `rimuc`
built-in layouts [header and footer
files](https://github.com/srackham/rimu/tree/master/src/rimuc/resources).
