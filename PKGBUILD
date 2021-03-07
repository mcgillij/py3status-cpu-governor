# Maintainer: Jason McGillivray < mcgillivray dot jason at gmail dot com>


pkgname=py3status-cpu-governor
pkgdesc="Python module for py3status to keep track of your cpu governor state"
pkgver=0.1.0
pkgrel=1
arch=('any')
license=('GPL2')
depends=('python' 'py3status')
makedepends=('python-setuptools')
url="https://github.com/mcgillij/py3status-cpu-governor"
source=("py3status-cpu-governor-0.1.0.tar.gz")
md5sums=('4ce0f257c3f355d28f924d583a336dee')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  python setup.py build
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  python setup.py install --prefix=/usr --root="$pkgdir"
} 
