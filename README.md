# counsel-dash

Browse [Dash](http://www.kapeli.com/dash) docsets using [Ivy](https://github.com/abo-abo/swiper).

## Installation

### MELPA

Pending.

### Source

Make sure `counsel-dash.el` is in your `load-path` and then:

```elisp
(require 'counsel-dash)
```

## How it works

This is a simple wrapper around [helm-dash](https://github.com/areina/helm-dash/), of which you should check out for
implementation details.

Unfortunately [helm-dash](https://github.com/areina/helm-dash/) depends on helm, so this package also implicitly depends
on helm - even though helm isn't really necessary. In the future, helm-dash may be decoupled into a separate library
that provides dash capabilities only. At that point we will switch over to the new library - the API will remain unchanged.

## Configuration



## License

See [LICENSE](https://github.com/nathankot/counsel-dash/blob/master/LICENSE)
