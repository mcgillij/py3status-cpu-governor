# Maintainer: Jason McGillivray < mcgillivray dot jason at gmail dot com>


pkgname=py3status-cpu-governor
pkgdesc="Python module for py3status to keep track of your cpu governor state"
pkgver=0.1.6
pkgrel=1
arch=('any')
license=('MIT')
depends=('python' 'py3status')
makedepends=('python-setuptools' 'python-poetry' 'python-build' 'python-installer')
url="https://github.com/mcgillij/py3status-cpu-governor"
source=("https://github.com/mcgillij/py3status-cpu-governor/releases/download/$pkgver/py3status_cpu_governor-$pkgver.tar.gz")
#source=("py3status_cpu_governor-$pkgver.tar.gz")
md5sums=('d69e7bcab8f3094d67e098878b4e21f9')

build() {
  cd "$srcdir/py3status_cpu_governor-$pkgver"
  python -m build --wheel --no-isolation
}

package() {
  cd "$srcdir/py3status_cpu_governor-$pkgver"
  python -m installer --destdir="$pkgdir" dist/*.whl
} 
