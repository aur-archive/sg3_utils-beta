# Contributor : Dmitry Nosachev <quartz64@gmail.com>
# Maintainer: Dmitry Nosachev <quartz64@gmail.com>

pkgname=sg3_utils-beta
_prname=sg3_utils
pkgver=1.33b6r429
pkgrel=1
pkgdesc="Generic SCSI utilities"
arch=('i686' 'x86_64')
url="http://sg.danny.cz/sg/sg3_utils.html"
license=('BSD')
depends=('glibc')
provides=('sg3_utils')
conflicts=('sg3_utils')
options=('!libtool')
source=(http://sg.danny.cz/sg/p/${_prname}-${pkgver}.tgz)
md5sums=('065f994d620a900f0bc78587b9f0eccf')

build() {
	cd ${srcdir}/${_prname}-${pkgver}
	./configure --prefix=/usr
	make || return 1
	install -D -m644 BSD_LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
	make DESTDIR=${pkgdir} install || return 1
}
