# Elm SPA Template

Simple SPA template.  Structured to handle each page as a separate module in a similar fashion to a MVC app. Made to be the bare minimum of a SPA but with a structure that can scale well.

This is basically a trimmed down version of the Elm [Real World](https://github.com/rtfeldman/elm-spa-example "Real World") example from Richard Feldman. So all credit to him.

Modified to serve from directory public

```
Structure:
.
├── LICENSE
├── README.md
├── elm-package.json
├── public
│   └── index.html
│   ├── elm.js <=== created by compilation
└── src
    ├── Main.elm
    ├── Page
    │   ├── About.elm
    │   ├── Error.elm
    │   ├── Home.elm
    │   └── NotFound.elm
    ├── Route.elm
    ├── Util.elm
    └── View
        └── Page.elm
```

## Get It Running

**1.** Install `elm` and `elm-live`:

> npm install -g elm elm-live

**2.** Build and run:

> elm-live --output=public/elm.js --dir=public src/Main.elm --pushstate --open

## Tests

**1.** Install `elm-test`:

> npm install -g elm-test

**2.** Initialize:

> elm-test init

**3.** Run and watch for changes:

> elm-test --watch

See [elm-test repo](https://github.com/elm-community/elm-test) for how to write tests.

## Why

The original [els-spa-template](https://github.com/simon-larsson/elm-spa-template.git) is a quick way to bootstrap an SPA but places index.html in the root directory. I prefer to keep static assets in a subdirectory named public. This fork simply moves index.html to public/index.html and invokes elm-live to build accordingly.

## Credits

https://github.com/simon-larsson/elm-spa-template.git
https://github.com/rtfeldman/elm-spa-example.git

