# Maintainer: Jameson Pugh <imntreal@gmail.com>
 
pkgname=onedrive
pkgver=1.0
pkgrel=1
pkgdesc="Free OneDrive client written in D"
arch=('i686' 'x86_64')
url="https://github.com/skilion/onedrive"
license=('GPL3')
depends=('dmd' 'curl' 'sqlite')
source=("https://github.com/skilion/onedrive/archive/v${pkgver}.tar.gz")
sha256sums=('ebec4b131806f0173dc6e1aee90639b3152d4819db3b06d0d7a7f82b3cc7d4bf')
 
build() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  make
}
 
package() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  install -dm 755 "${pkgdir}/bin"
  install -dm 755 "${pkgdir}/etc/onedrive"
  install -m 755 onedrive "${pkgdir}/bin/"
  install -m 622 onedrive.conf "${pkgdir}/etc/onedrive/"
}
 
# vim:set ts=2 sw=2 et:
