pkgname=ragel
pkgver=6.9
pkgrel=2
pkgdesc="Compiles finite state machines from regular languages into executable C, C++, Objective-C, or D code."
arch=('i686' 'x86_64')
url="http://www.complang.org/ragel/"
license=('GPL')
depends=('gcc-libs')
source=("http://fossies.org/linux/misc/$pkgname-$pkgver.tar.gz")
md5sums=('0c3110d7f17f7af4d9cb774443898dc1')

build() {
  cd "$srcdir/$pkgname-$pkgver"

  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"

  make DESTDIR="$pkgdir/" install
  install -m0644 -D ragel.vim "$pkgdir"/usr/share/vim/vimfiles/syntax/ragel.vim
}
