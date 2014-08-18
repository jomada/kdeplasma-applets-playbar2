pkgname=kdeplasma-applets-playbar
pkgver=0.6.1
pkgrel=1
pkgdesc="Client Mpris2, allows you to control your favorite media player."
arch=('x86_64')
url="http://kde-apps.org/content/show.php?action=content&content=165396"
license=('GPL')
depends=('kde-workspace')
makedepends=('gcc' 'cmake' 'automoc4')
source=("https://github.com/audoban/PlayBar/archive/v0.6.1/PlayBar-$pkgver.tar.gz")
md5sums=('659047be95d21ae001a6e9d02bdec9c0')

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

