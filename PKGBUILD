## Maintainer: Mariusz Libera <mariusz.libera@gmail.com>
## Contributor: Joshua Stiefer <facedelajunk@gmail.com>
pkgname=libtermkey
pkgver=0.17
pkgrel=2
pkgdesc="Library for easy processing of keyboard entry from terminal-based programs"
arch=('i686' 'x86_64')
url="http://www.leonerd.org.uk/code/libtermkey/"
license=('MIT')
depends=('unibilium')
source=("http://www.leonerd.org.uk/code/${pkgname}/${pkgname}-${pkgver}.tar.gz")
sha256sums=('68949364ed5eaad857b3dea10071cde74b00b9f236dfbb702169f246c3cef389')

build() {
	cd "${pkgname}-${pkgver}"
	make
}

package() {
	cd "${pkgname}-${pkgver}"
	make PREFIX=/usr DESTDIR="${pkgdir}" install

	install -D -m 644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
