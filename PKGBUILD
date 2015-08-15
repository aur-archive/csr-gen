# Maintainer: Michael Düll <mail@akurei.me> PGP-Key: AAAEE882

pkgname="csr-gen"
pkgver=1
pkgrel=4
pkgdesc="Script from CaCert.org to simplify the generation of Certificate Signing Requests (CSR)."
arch=('any')
url="http://wiki.cacert.org/CSRGenerator"
license=('BSD')
depends=('openssl')
source=('csr-gen')

package() {
  cd "$srcdir/"

  # Make directories
  install -d ${pkgdir}/usr/bin/
  install -d ${pkgdir}/usr/share/licenses/csr-gen/

  # Install "binary"
  install -Dm 755 csr-gen ${pkgdir}/usr/bin/

  # License
  head -n 27 csr-gen | tail -n 25 | cut -d '#' -f 2- | cut -c 2- > ${pkgdir}/usr/share/licenses/csr-gen/LICENSE
  chmod 644 ${pkgdir}/usr/share/licenses/csr-gen/LICENSE
}

# vim:set ts=2 sw=2 et:
sha512sums=('dbe175b9d42aac5bc7b012c00dcde30e9b8820eeaafa8b2567eb956a3002e4e8eeeb6073c46ea43c16f6c1832f65080850823434148e87a8bd4f72dfab582fb1')
