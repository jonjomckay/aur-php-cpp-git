# Maintainer: Jonjo McKay <jonjo@jonjomckay.com>
pkgname=php-cpp-git
pkgver=20140322
pkgrel=1
pkgdesc="Library to build PHP extensions with C++"
arch=('i686' 'x86_64')
url="http://www.php-cpp.com"
license=('Apache')
depends=('php')
conflicts=('php-cpp')
options=('strip' 'ccache')
source=("$pkgname::git+https://github.com/CopernicaMarketingSoftware/PHP-CPP.git")
md5sums=('SKIP')

build() {
	cd "$srcdir/${pkgname}"
	make PHP_DIR=/usr/include/php
}

package() {
	cd "$srcdir/${pkgname}"
	mkdir -p "$pkgdir/usr/lib"
	make INSTALL_PREFIX="$pkgdir/usr" install
}
