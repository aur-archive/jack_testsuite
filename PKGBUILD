# Contributor: Markus Härer <markus.haerer@gmx.net>
pkgname=jack_testsuite
pkgver=1.0
pkgrel=1
pkgdesc="A pimped up version of the jacktest tool from ardour"
arch=('i686' 'x86_64')
url="http://wiki.linuxproaudio.org/index.php/jack:dsp_benchmark"
license=('GPL')
depends=('gcc-libs' 'jack')
source=(http://www.linuxproaudio.org/src/jack_testsuite.tar.bz2)
md5sums=('1336463ade6ec0d61750f06edcf0a4b0')

build() {
  cd "$srcdir/$pkgname"

  make || return 1
}

package() {
  cd "$srcdir/$pkgname"
  
  mkdir -p $pkgdir/usr/bin

  install -m 755 jack_latency $pkgdir//usr/bin
  install -m 755 jack_bench $pkgdir/usr/bin
}

