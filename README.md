# counsel-dash

[![Melpa Status](http://melpa.milkbox.net/packages/counsel-dash-badge.svg)](http://melpa.milkbox.net/#/counsel-dash)

Browse [Dash](http://www.kapeli.com/dash) docsets using [Ivy](https://github.com/abo-abo/swiper).

## Installation

### MELPA

```
M-x package-install RET counsel-dash RET
```

### Source

Make sure `counsel-dash.el` is in your `load-path` and then:

```lisp
(require 'counsel-dash)
```

## How it works

This is a simple wrapper around [helm-dash](https://github.com/areina/helm-dash/), of which you should check out for
implementation details.

Unfortunately [helm-dash](https://github.com/areina/helm-dash/) depends on helm, so this package also implicitly depends
on helm - even though helm isn't really necessary. In the future, helm-dash may be decoupled into a separate library
that provides dash capabilities only. At that point we will switch over to the new library - the API will remain unchanged.

## Configuration

You'll find most of the available functions and configuration variables are
exactly the same as [helm-dash](https://github.com/areina/helm-dash/) with a
different prefix (`s/helm-dash/counsel-dash/`.) This is because they are simply
aliases to the helm-dash equivalents.

### Install docsets

```
M-x counsel-dash-install-docset
```

### Setup default docsets

```lisp
(setq counsel-dash-common-docsets '("Javascript" "HTML"))
```

### Setup mode-specific docsets

```lisp
(add-hook 'emacs-lisp-mode-hook (lambda () (setq-local counsel-dash-docsets '("Emacs Lisp"))))
(add-hook 'ruby-mode-hook (lambda () (setq-local counsel-dash-docsets '("Ruby"))))
```

### Other options

```lisp
(setq counsel-dash-docsets-path "~/.docset")
(setq counsel-dash-docsets-url "https://raw.github.com/Kapeli/feeds/master")
(setq counsel-dash-min-length 3)
(setq counsel-dash-candidate-format "%d %n (%t)")
(setq counsel-dash-enable-debugging nil)
(setq counsel-dash-browser-func 'browse-url)
(setq counsel-dash-ignored-docsets nil)
```

## Usage

```
M-x counsel-dash
```

## License

See [LICENSE](https://github.com/nathankot/counsel-dash/blob/master/LICENSE)
