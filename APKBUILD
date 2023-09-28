# Maintainer: Yunus Emre YOLDAŞ <yoldas.emre@anticverse.com>
pkgname=homeless
pkgver=99999
pkgrel=0
_commit=79b2cbcd4491a85b8d655ea5f23352d7e4b99227
pkgdesc="A sahibinden.com scraper bot for telegram written in C++"
url="https://github.com/gAtrium/homeless"
arch="all"
license="MIT"
depends=""
makedepends="cmake curl-dev openssl-dev nlohmann-json tgbot-cpp boost-dev"
source="
	$pkgname-$_commit.tar.gz::https://github.com/gAtrium/homeless/archive/$_commit.tar.gz
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
c3353d190570496a2507991cdf94c39872a06a1b962cd4815462b532fe9a08c37e7032ad47117d3d882635a68183251528a28efbab7aad5958d2f5519d430a36  homeless-79b2cbcd4491a85b8d655ea5f23352d7e4b99227.tar.gz
"
