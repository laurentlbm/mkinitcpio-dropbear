pkgname=mkinitcpio-dropbear
pkgver=0.1.0
pkgrel=1
pkgdesc="Archlinux mkinitcpio hook to install and enable the dropbear daemon in early userspace"
arch=('any')
url="https://github.com/laurentlbm/mkinitcpio-dropbear"
license=('GPL3')
depends=('dropbear' 'psmisc')
optdepends=('openssh: Allows the use of the same host keys used for normal access' 'mkinitcpio-netconf: Network interface configuration' 'mkinitcpio-ppp: PPP interface configuration')
source=("${pkgname}-${pkgver}.tar.gz::$url/archive/v$pkgver.tar.gz")
sha512sums=('d6f2bfd3287b07c331511518390b4e7261aa984f14d49ddde46140622639cd2790103c0142fd68aa3d76ef8041ce8f521b02d34f32387b4bdecd7cbaa0076d24')

package() {
  install -Dm644 "$srcdir/$pkgname-$pkgver/dropbear_hook"      "$pkgdir/usr/lib/initcpio/hooks/dropbear"
  install -Dm644 "$srcdir/$pkgname-$pkgver/dropbear_install"   "$pkgdir/usr/lib/initcpio/install/dropbear"
  install -Dm644 "$srcdir/$pkgname-$pkgver/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
