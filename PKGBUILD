# Maintainer: Guillaume Horel <guillaume.horel@gmail.com>
pkgname=python-branca
_pkgname=branca
pkgver=0.3.0
pkgrel=1
pkgdesc="Generate html+js with Python."
arch=('any')
url="https://github.com/python-visualization/branca"
license=('MIT')
checkdepends=('python-nose' 'python-selenium' 'geckodriver')
depends=('python' 'python-jinja')
options=(!emptydirs)
source=("https://github.com/python-visualization/branca/archive/v$pkgver.tar.gz")
sha256sums=('f9932fa59998224439f4f8e7bcc17a8e613f4776945ef0ddb9152d23ea0c0633')

check() {
    cd "$srcdir/$_pkgname-$pkgver"
    nosetests
}

package() {
  cd "$srcdir/$_pkgname-$pkgver"
  python setup.py install --root="$pkgdir/" --optimize=1
  install -D -m644 LICENSE.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.txt"
}
