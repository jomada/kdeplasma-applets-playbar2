pkgname=kdeplasma-applets-playbar
pkgver=0.7
pkgrel=1
pkgdesc="Client Mpris2, allows you to control your favorite media player."
arch=('x86_64')
url="http://kde-apps.org/content/show.php?action=content&content=165396"
license=('GPL')
depends=('kdelibs')
makedepends=('gcc' 'cmake' 'automoc4')
source=("https://github.com/audoban/PlayBar/archive/v0.7/PlayBar-$pkgver.tar.gz")
md5sums=('adc3512aae6f57d45236c4dccc68e11e')

build() {
cd $srcdir/PlayBar-${pkgver}
mkdir build && cd build
cmake -DCMAKE_INSTALL_PREFIX=/usr ..
make
}
package() {
cd $srcdir/PlayBar-${pkgver}/build
make DESTDIR="$pkgdir/" install
}

