 #Maintainer: Sven-Hendrik Haase 
pkgname=RF24
pkgver=600.973533d
pkgrel=1
pkgdesc="A library for interfaceing with nRF24 2.4Ghz radio module"
arch=('armv7h')
url="https://github.com/TMRh20/RF24"
license=('AGPL3')
depends=( )
makedepends=( )
optdepends=( )
source=("git+https://github.com/TMRh20/RF24")
md5sums=('SKIP')
sha1sums=('SKIP')

#prepare() {
 # nothing
#}

build() {
  cd RF24
  ./configure --prefix=/usr --ldconfig=''
  make -j4
}

package() {
  cd RF24
  make LIB_DIR="$pkgdir/usr/lib" HEADER_DIR="$pkgdir/usr/include" install
  rm $pkgdir/usr/include/printf.h
}

pkgver() {
	cd $srcdir
	echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}

 