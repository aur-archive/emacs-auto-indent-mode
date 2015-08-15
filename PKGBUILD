# Contributor: Nathan Owe <ndowens.aur at gmail dot com>
# Contributor: Stefan Husmann <stefan-husmann@t-online.de>
# Maintainer:  Thomas Etcheverria <tetcheve at gmail dot com>

pkgname=emacs-auto-indent-mode
pkgver=0.126
pkgrel=1
pkgdesc="Auto indent mode for Emacs"
arch=('any')
url="http://emacswiki.org/emacs/"
license=('GPL')
depends=('emacs')
source=(http://www.emacswiki.org/emacs/download/auto-indent-mode.el)
md5sums=('e469cd2252c3ceb3db023dbc0248091c')
install=$pkgname.install


build() {
  cd "$srcdir/"
  emacs -batch -f batch-byte-compile auto-indent-mode.el
}

package() {
  cd "$srcdir/"
  install -Dm644 auto-indent-mode.el \
    $pkgdir/usr/share/emacs/site-lisp/auto-indent-mode.el
  install -Dm644 auto-indent-mode.elc \
    $pkgdir/usr/share/emacs/site-lisp/auto-indent-mode.elc
}
