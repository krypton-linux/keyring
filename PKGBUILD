pkgname=krypton-keyring
pkgver=8a6c751
pkgrel=1
pkgdesc="Krypton Linux Keyring"
arch=('any')
url="https://krypton-linux.com"
license=('MIT')
install="${pkgname}.install"
source=('git+https://github.com/krypton-linux/keyring.git')
validgpgkeys=('88E913F2A69458547D7E96A0675E89BAE0754C86')
sha512sums=('SKIP')

pkgver() {
    cd "$srcdir/keyring"
    git rev-parse --short HEAD
}

package() {
    cd $srcdir/keyring
	make PREFIX=/usr DESTDIR=${pkgdir} install
}
