# Maintainer: 0xDEADCADE <0xDEADCADE@protonmail.com>

pkgname=ps4fancontrol-nogui
pkgver=1.0.0
pkgrel=1
pkgdesc="Adjust fan speeds based on the threshold temperature set"
arch=('any')
license=('LGPL')
conflicts=('ps4fancontrol')
provides=('ps4fancontrol')
url="https://github.com/0xDEADCADE/ps4fancontrol-nogui/"
depends=()
makedepends=('git')
source=("git+https://github.com/0xDEADCADE/$pkgname")
sha256sums=('SKIP')

build() {
  cd $pkgname
  make
}

package() {
  cd $pkgname
  install -d "$pkgdir"/usr/bin/
  install -m755 "$srcdir/$pkgname"/ps4fancontrol "$pkgdir"/usr/bin/ps4fancontrol
}
