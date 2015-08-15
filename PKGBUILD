# Maintainer: kusakata <shohei atmark kusakata period com>

pkgname=bmtape2
pkgver=20140321
pkgrel=2
pkgdesc="HITACHI BASIC MASTER Jr. Tape Converter"
arch=('i686' 'x86_64')
url="http://ver0.sakura.ne.jp/pc/"
license=('BSD')
depends=('glibc')
source=("http://ver0.sakura.ne.jp/pc/bmtape2src_${pkgver}.tgz")

build() {
	cd "${srcdir}/bmtape2"
	make
}

package() {
	cd "${srcdir}/bmtape2"
	install -Dm755 bmtape2 "${pkgdir}/usr/bin/${pkgname}"
	
	sed -n '/Copyright (c)/,/す。/p' readme.txt > LICENSE
	install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
	install -Dm644 readme.txt "${pkgdir}/usr/share/doc/${pkgname}/readme.txt"
}

md5sums=('634f465c311a693e92038d0892fa1542')
