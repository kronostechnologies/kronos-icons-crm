CRM SVG icons
=============

Here is the canonical source of the SVG icons of the Kronos CRM.

How is this used
----------------

This repo is used as a git submodule in the in the
`img/svg/symbols/icons/` repository of the CRM.

From the CRM project's root:

1. `git submodule add git@github.com:kronostechnologies/kronos-icons-crm.git ./img/svg/symbols/icons`
2. `git submodule update --init`

Pour `checked out` aux dernières versions des submodules :

* `git submodule update --recursive --remote`.

Then all those files must be concatenated and converted into
[symbols](http://devdocs.io/svg/element/symbol) in a single SVG
file. Right now, it is done with a grunt task called
`svg_symbols`. Behind that task there's the plugin
[grunt-svg-symbols](https://www.npmjs.com/package/grunt-svg-symbols).

### Ouput Example

The generated file is `./public/img/icons.svg`.

```
<svg class="svg-symbols visuallyhidden" xmlns="http://www.w3.org/2000/svg">
    <symbol id="ico-angle-down" viewBox="0 0 10 16">
        <path d="M9.598 6.571a.309.309 0 0 1-.089.205l-4.161 4.161c-.054.054-.134.089-.205.089s-.152-.036-.205-.089L.777 6.776c-.054-.054-.089-.134-.089-.205s.036-.152.089-.205l.446-.446a.29.29 0 0 1 .205-.089c.071 0 .152.036.205.089l3.509 3.509L8.651 5.92c.054-.054.134-.089.205-.089s.152.036.205.089l.446.446a.306.306 0 0 1 .089.205z" fill="currentColor"></path>
    </symbol>

    <symbol id="ico-cog" viewBox="0 0 16 16">
        <path d="M13.426 8c0-.839.517-1.5 1.294-1.954a7.18 7.18 0 0 0-.554-1.338c-.871.228-1.576-.113-2.169-.706-.593-.592-.774-1.297-.546-2.169a7.018 7.018 0 0 0-1.338-.553c-.454.776-1.276 1.292-2.114 1.292S6.34 2.056 5.885 1.28a6.945 6.945 0 0 0-1.337.553c.228.872.047 1.577-.547 2.169-.592.594-1.297.934-2.169.706-.228.422-.414.87-.553 1.338C2.055 6.5 2.571 7.161 2.571 8c0 .838-.516 1.659-1.292 2.114.14.467.325.915.553 1.338.872-.228 1.577-.047 2.169.546s.775 1.298.547 2.169c.422.228.87.414 1.338.554.454-.778 1.276-1.294 2.114-1.294s1.659.516 2.114 1.294a7.209 7.209 0 0 0 1.338-.554c-.228-.87-.047-1.575.546-2.169.593-.592 1.298-.933 2.169-.706a7.06 7.06 0 0 0 .554-1.338c-.778-.455-1.295-1.116-1.295-1.954zM8 10.922a2.922 2.922 0 1 1 0-5.843 2.922 2.922 0 0 1 0 5.843z" fill="currentColor"></path>
    </symbol>
    <!-- {Etc...} -->
</svg>
```

### Usage

```
<button class="metasearchbar__submit">
  <span class="visuallyhidden">{{ _('METASEARCH_SUBMIT') }}</span>

  <svg class="metasearchbar__ico">
    <use xlink:href="#ico-magnifying-glass"></use>
  </svg>
</button>
```

For the SVG contributors (designers)
------------------------------------

*Soon*
