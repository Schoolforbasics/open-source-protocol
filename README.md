# Open Source Protocol

###About

The Open Source Protocol is a way of telling developers where to access the source code for your website, if the source code is hosted in an open source repository on the public internet.

The OS Protocol uses metatags. To include an open source metatag on your website, simply add `<meta />` tags for the following properties:

* `os:repo` - This should be a link to the repository web page, for instance the project page on GitHub, Bitbucket, or Sourceforge.
* `os:rcs_type` - This should be the name of the revision control system used, for instance Git, Mercurial, Bazaar.
* `os:src` - This is the repository url that can be used to obtain a copy of the source.

This is not a place to link to code that is described on your website; rather, this is for the code _for the actual website_. That way, if anyone reading your website sees an error - a spelling mistake, broken CSS, etc. - or something they want to examine - a cool paralax library, etc. - they can quickly fetch the source code.

The `os` protocol is loosely based on the [Open Graph protocol](http://ogp.me/), which in turn is based on [RDFa](https://en.wikipedia.org/wiki/RDFa). `os` stands for "open source".

The following `link` element must be added in order to adhere to the standard. This is similar to the now deprecated `profile` attribute, which used to go into the `<HEAD />`: `<link rel="profile" href="https://github.com/RichardLitt/open-source-protocol/" />`. Note: This URI may change if this protocol is accepted enough to warrant a new domain. 

###Example

```html
<link rel="profile" href="http://osprotocol.com" />
<meta property="os:repo" content="https://github.com/RichardLitt/open-source-protocol" />
<meta property="os:rcs_type" content="git" />
<meta property="os:src" content="git@github.com:RichardLitt/open-source-protocol.git" />
```

###Optional tags

Other tags that can be used:

* `os:issue` - This links to a place to report issues for the website.
* `os:commit` - This is the commit id that the current site is based upon, as that may not always be the same as HEAD.
* `os:branch` - This is the branch where the live code for the website lives.

####Examples 

```html
<meta property="os:issue" content="https://github.com/RichardLitt/open-source-protocol/issues" />
<meta property="os:commit" content="1sda73d" />
<meta property="os:branch" content="gh-pages" />
```

###Shields

For use in the repository, to show your compliance and spread the word:

![passing](https://img.shields.io/badge/OSMT-passing-green.svg) https://img.shields.io/badge/OSMT-passing-green.svg  
![failing](https://img.shields.io/badge/OSMT-failing-red.svg) https://img.shields.io/badge/OSMT-failing-red.svg

###Contribute

This is a work in progress. Please open an [issue](https://github.com/RichardLitt/open-source-protocol/issues) to discuss how the Open Source Protocol can be improved. PRs are encouraged!

To automatically copy `README.md` from `master` to `gh-pages`, use the hook on `gh-pages` in `dev`. (_Note: It doesn't like `git add -p`_).
