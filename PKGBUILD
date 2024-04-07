# Maintainer: Matthew Phillip Cooper <matthew@coopertronic.co.uk>

pkgname=ctos-skel
_destname1="/etc"
pkgver=1.r12.963dbb0
pkgrel=1
pkgdesc="This installs the skel folder in etc that is used to generate a new user."
arch=('any')
url="https://github.com/Coopertronic/$pkgname.git"
license=('GPL3')
makedepends=('git')
depends=()
conflicts=()
provides=("${pkgname}")
options=(!strip !emptydirs)
source=("git+$url")
sha256sums=('SKIP')

pkgver() {
    cd "${srcdir}/${pkgname}"
    printf "1.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    install -dm755 ${pkgdir}${_destname1}
    cp -r ${srcdir}/${pkgname}${_destname1}/* ${pkgdir}${_destname1}
}
