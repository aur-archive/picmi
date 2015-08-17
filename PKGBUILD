# Maintainer: schuay <jakob.gruber@gmail.com>

pkgname=picmi
pkgver=1.9.95
pkgdesc='A nonogram logic game for KDE'
pkgrel=1
arch=('i686' 'x86_64')
url='https://github.com/schuay/picmi'
license=('GPL')
depends=('qt' 'kdelibs' 'kdegames-libkdegames')
makedepends=('cmake' 'automoc4')
source=("https://github.com/downloads/schuay/${pkgname}/${pkgname}-$pkgver.tar.bz2")

build() {
  cd ${srcdir}/${pkgname}

  rm -rf ./build
  mkdir build && cd build
  cmake -DCMAKE_INSTALL_PREFIX="/usr" ..
  make
}

package() {
  cd ${srcdir}/${pkgname}/build

  make DESTDIR="${pkgdir}" install
}

md5sums=('2fd5ed53fc711674352bb0a974bb0128')
