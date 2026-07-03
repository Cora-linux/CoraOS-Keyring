pkgname=coraos-keyring
pkgver=1
pkgrel=1
pkgdesc="CoraOS PGP keyring"
arch=('any')
license=('GPL')
depends=('pacman')
install=$pkgname.install

source=('coraos.gpg'
        'coraos-revoked'
        'coraos-trusted')

b2sums=('c2e0dfb5210bb66569c1d1c5e6f3c9a9b029144be8750147cbf252d68bd4033f1c6a9414deaca4e93e690e578ca7c8b5b1d9cfc0e42044eb082de3a63e30ad26'
        '786a02f742015903c6c6fd852552d272912f4740e15847618a86e217f71f5419d25e1031afee585313896444934eb04b903a685b1448b755d56f701afe9be2ce'
        '4774f207a80c71075a28b42873acab52fb251482c4131172d5d55bdb07ca3e9b281a6f281dc765b9af9e807d51ab9b70ee507da30fb764c379e857ac03ab13bd')

package() {
    install -Dm644 "$srcdir/coraos.gpg" \
        "$pkgdir/usr/share/pacman/keyrings/coraos.gpg"

    install -Dm644 "$srcdir/coraos-revoked" \
        "$pkgdir/usr/share/pacman/keyrings/coraos-revoked"

    install -Dm644 "$srcdir/coraos-trusted" \
        "$pkgdir/usr/share/pacman/keyrings/coraos-trusted"
}
