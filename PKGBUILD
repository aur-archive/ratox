# Maintainer: Håvard Pettersson <mail@haavard.me>

pkgname=ratox
pkgver=0.2.1
pkgrel=1

pkgdesc='FIFO based Tox client'
arch=('i686' 'x86_64')
url='http://ratox.2f30.org'
license=('MIT')

depends=('tox-git')

source=("http://dl.2f30.org/releases/${pkgname}-${pkgver}.tar.gz")
md5sums=('b86b2c5330fa3e1720bf3419c3d72e17')
sha256sums=('25ea4e7e286d23ca4fe99e0619c384fc6b371178e8877681b382d94dd958a9ba')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make PREFIX=/usr DESTDIR="${pkgdir}" install
  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

