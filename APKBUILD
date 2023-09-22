# Maintainer: Yunus Emre YOLDAŞ <yoldas.emre@anticverse.com>
pkgname=homeless
pkgver=99999
pkgrel=0
_commit=7c737c6640d436ddd998a55790f4b245a7d58fdd
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
757f3dc288cc84db9cac5533dcf5c0300e63f2987433da889fcbbe3150d207f60eb3ebbb05420521bd9e1ca37fefacd093efe8567c082f66c0fea3450f460d7f  homeless.tar.gz
"
