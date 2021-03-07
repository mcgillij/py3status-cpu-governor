# Maintainer: Jason McGillivray < mcgillivray dot jason at gmail dot com>


pkgname=py3status-cpu-governor
pkgdesc="Python daemon for controlling the fans on amdgpu cards"
pkgver=0.1.0
pkgrel=1
arch=('any')
license=('GPL2')
depends=('python' 'py3status')
makedepends=('python-setuptools')
url="https://github.com/mcgillij/amdfan"
source=("py3status-cpu-governor-0.1.0.tar.gz")
#source=("https://github.com/mcgillij/amdfan/releases/download/0.1.7/amdfan-0.1.7.tar.gz")
md5sums=('4ce0f257c3f355d28f924d583a336dee')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  python setup.py build
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  python setup.py install --prefix=/usr --root="$pkgdir"
} 
