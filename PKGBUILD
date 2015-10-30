pkgname=kdeplasma-applets-playbar2
_name=PlayBar2
pkgver=2.2
pkgrel=1
pkgdesc="Mpris2 Client for Plasma5"
arch=('x86_64')
url="https://github.com/audoban/PlayBar2"
license=('GPL')
depends=('plasma-framework' 'plasma-workspace' 'kdeclarative' 'kglobalaccel'
    'kconfigwidgets' 'kxmlgui' 'kwindowsystem')
makedepends=('kdoctools' 'extra-cmake-modules')
source=("https://github.com/audoban/${_name}/archive/v${pkgver}.tar.gz")
md5sums=('e3e69ab4719764856033247ef4170942')

prepare() {
    mkdir -p build
}

build() {
    cd build
    cmake -DCMAKE_BUILD_TYPE=Release \
        -DCMAKE_INSTALL_PREFIX=/usr \
        -DLIB_INSTALL_DIR=lib \
        -DKDE_INSTALL_USE_QT_SYS_PATHS=ON \
        ../${_name}-${pkgver}
    make
}

package() {
    cd build
    make DESTDIR="$pkgdir" install
}
