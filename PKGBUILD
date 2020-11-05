# Maintainer: Jiachen Yang <farseerfc@gmail.com>
pkgname=systemd-report-entropy
pkgver=1
pkgrel=1
pkgdesc="help to diagnose shutdown sequence for systemd"
arch=(any)
url="http://github.com/farseerfc/systemd-report-entropy"
license=('custom:BSD')
depends=()
source=("$pkgname"
    "$pkgname.service"
    'LICENSE'
)
sha512sums=('883b12b23cad21f620fb10e6f682390d155da65f41517701296793e7ad4ca16e55547b78d3fb06dd697a261e5f236e5d96e6d6c539d16ed3a7b52f890066ac59'
            'ab00ff35e6e74f90589587c44d3efc4584f0d5d40e7767ee2fc982f2b20f0656dfbb58b3c3a8103a32538a28bb08dd15087114aae0b1f6f73a12b6073d32c99f'
            '26faec19537be2d4dad83e16a3557d1ab20f71a3f66abbfb8725e7fd9233fef6df2c21c81f5c48c48963746d8b319483615a25ae1fb49f8b3667f30e6b1418ec'
            '2ee770dce7cbf95d07b49e24522c6be2d7dd8f3cbe88097d6b27a9ea05052525ef58ef6c2f95bf09bcbc38db46918098faf13655c0f6853b3057dac9ec10e6bb')

package() {
    install -Dm755 $pkgname "$pkgdir/usr/bin/$pkgname"
    install -Dm644 $pkgname.service "$pkgdir/usr/lib/systemd/system/$pkgname.service"
    install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
