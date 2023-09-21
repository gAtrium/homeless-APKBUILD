# Maintainer: Yunus Emre YOLDAŞ <yoldas.emre@anticverse.com>
pkgname=homeless
pkgver=99999
pkgrel=0
_commit=ba538e94b6bd738a93b66fc19ef1ffe112757642
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
2da2286abc1fe0dbc111b563d3a885bd145be96113ffcf9a77424a70b87b68f9e690c63da33f951ee77de4120c2545188f94546244552c3974c65e5fae075ba4  homeless.tar.gz
"
