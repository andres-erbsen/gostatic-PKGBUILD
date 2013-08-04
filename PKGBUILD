# Maintainer: Andres Erbsen <andres@krutt.org>

pkgname=gostatic-git
progname=gostatic
pkgver=1.3
pkgrel=1
pkgdesc="Fast, dependency-tracking static site generator"
arch=('x86_64' 'i686')
license=('ISC')
makedepends=('go')
options=('!strip' '!emptydirs')
pkgimportpath="github.com/piranha/gostatic"

build() {
  source /etc/profile.d/go.sh
  export GOPATH="$srcdir"
  go get -u "$pkgimportpath"
}

package() {
  install -Dm755 "$srcdir/bin/$progname" "$pkgdir/usr/bin/$progname"
  install -Dm644 "$srcdir/src/$pkgimportpath/LICENSE" "$pkgdir/usr/share/licenses/$progname/LICENSE"
}

# vim:set ts=2 sw=2 et:
