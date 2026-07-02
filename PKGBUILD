# Maintainer: FusionTech <support@coraos.org>

pkgbase=coraos-keyring
pkgname=(coraos-keyring)
pkgver=20260726
pkgrel=1
pkgdesc='CoraOS PGP keyring'
arch=('any')
url='https://github.com/Cora-linux/CoraOS-Keyring'
license=('GPL-3.0')
makedepends=('git' 'python' 'sequoia-sq' 'pkgconf' 'systemd')
checkdepends=('python-coverage' 'python-pytest')

source=("CoraOS-Keyring::git+https://github.com/Cora-linux/CoraOS-Keyring.git#tag=${pkgver}")
b2sums=('SKIP')
sha256sums=('SKIP')

validpgpkeys=('361EC3F1B76210CE2ABB7BE002552EA95DC06E87')

build() {
  cd CoraOS-Keyring/
  make build
}

check() {
  cd CoraOS-Keyring/
  make check
}

package_coraos-keyring() {
  install=coraos.install
  depends=('pacman')

  cd CoraOS-Keyring/
  make PREFIX='/usr' DESTDIR="${pkgdir}" install
}
