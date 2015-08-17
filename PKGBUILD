# Submitter: Colin Duquesnoy <colin.duquesnoy@gmail.com>
# Maintainer: Colin Duquesnoy <colin.duquesnoy@gmail.com>
pkgbase=open-cobol-ide
pkgname=('open-cobol-ide')
pkgver=4.6.2
_pkgver=4.6.2
pkgrel=0
arch=('any')
url="https://github.com/OpenCobolIDE/OpenCobolIDE"
license=('GPL')
pkgdesc="Simple and lightweight COBOL IDE"
depends=('python')
makedepends=('python-setuptools')
source=("https://github.com/OpenCobolIDE/OpenCobolIDE/archive/${_pkgver}.tar.gz")
depends=('python'
         'python-pyqt5'
         'python-qdarkstyle'
         'python-pyqode.cobol'
         'open-cobol')
md5sums=('7ea550e14b160f3d4c1434a99f229e6f')

build() {
   cd "$srcdir/OpenCobolIDE-${_pkgver}"
}

package() {
    cd "$srcdir/OpenCobolIDE-${_pkgver}"
    python3 setup.py install --root="$pkgdir/" --optimize=1
    install -D -m644 "$srcdir/OpenCobolIDE-${_pkgver}/LICENSE" $pkgdir/usr/share/licenses/$pkgname/LICENSE
}
