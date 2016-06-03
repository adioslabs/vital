# Vital

A minimally invasive CSS framework for modern web applications.

- Vital is a reverse approach to "everything and the kitchen sink" CSS frameworks.
- Built with Sass and Slim for readability and maintainability.
- No ridiculous amounts of classes or nesting. No excessively buried code.
- Written almost entirely in em values, allowing for easy and consistent scaling.
- Small:

|                | Size  | Gzipped |
|:---------------|:------|:--------|
| CSS Framework  | 22 KB | 6 KB    |
| Icons (.svg)   | 3 KB  | 1 KB    |
| Icons (.eot)   | 2 KB  |         |
| Icons (.ttf)   | 2 KB  |         |
| Icons (.woff)  | 2 KB  |         |
| Javascripts    | 0     |         |
| Total          | 31 KB |         |

## Setup / Installation

### Quickest (Compiled)

Import into stylesheet or as a stylesheet link tag:

`https://cdn.rawgit.com/doximity/vital/master/releases/v1.1.2/stylesheets/vital.min.css`

### Recommended (Source)

`https://github.com/doximity/vital/tree/master/source/stylesheets`

Vital works best when manipulated directly. Download or copy the `.sass` files into your project. This installation method is preferred if you want to develop your own unique branding while keeping code output to a minimum. One possible caveat to this method is you sacrifice future upgradability as you may encounter breaking changes.

#### File Structure

```sass
// If you are using rails
// @import sprockets

// Vendor
@import normalize

// Components
@import variables
@import icons
@import grid

@import base
@import buttons
@import footer
@import forms
@import header
@import heroes
@import loaders
@import notice
@import pagination
@import tables
@import tabs
@import helpers

// Customizations
@import custom
```

### Packages

A Ruby gem and npm package installation options are in the works.

## Development Installation

Vital is built using a simple static generator: https://middlemanapp.com/

- Clone: `https://github.com/doximity/vital`
- In your terminal, run `bundle`
- To start your server, run `middleman` then navigate to http://localhost:4567

#### Building the Output

- `bundle exec rake build`

#### Compiling Font Icons

To compile font icons, you must first install FontForge and the Font Custom gem.

```bash
# On Mac
# Requires Ruby 1.9.2+, FontForge with Python scripting
brew install fontforge --with-python
brew install eot-utils
```

After installation is complete, run `bundle exec rake vital:compile_fonts`.

## Publishing to GitHub Pages

Publishing to `gh-pages` is done automatically by running `bundle exec rake publish`

## Reporting Issues and Suggestions

Please submit GitHub issues for problems with the library. Also, feel free to submit a pull-request with suggested changes.
