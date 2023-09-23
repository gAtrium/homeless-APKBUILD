# Maintainer: Yunus Emre YOLDAŞ <yoldas.emre@anticverse.com>
pkgname=homeless
pkgver=99999
pkgrel=0
_commit=9ad59c68981d84b3bdf736b69c51b37180c3446a
pkgdesc="A sahibinden.com scraper bot for telegram written in C++"
url="https://github.com/gAtrium/homeless"
arch="all"
license="MIT"
depends=""
makedepends="cmake curl-dev openssl-dev nlohmann-json tgbot-cpp boost-dev"
source="
	$pkgname.tar.gz::https://github.com/gAtrium/homeless/archive/$_commit.tar.gz
	"

build() {
  cd "homeless-$_commit"
  cmake -DCMAKE_INSTALL_PREFIX=/usr .
  make
}

package() {
  cd "src/homeless-$_commit"
  make DESTDIR="$pkgdir" install
}
sha512sums="
3ed5359c32ac8dd58d92213f0be97f3270fa457b556387b77c9b5734206b9670eb6492461f35f3c1e3f706c793a3363e8e52fd9d45d7fce3142d305f0c9e586f  homeless.tar.gz
"
