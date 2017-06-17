# Maintainer: Vyacheslav Konovalov <vyachkonovalov@gmail.com>
# Contributor: Damian Nowak <damian@nowaker.net>

pkgname=robomongo-bin
_pkgver=1.1.1
pkgver=${_pkgver/-/_}
pkgrel=1
pkgdesc='Shell-centric cross-platform open source MongoDB management tool'
arch=('x86_64')
url='https://robomongo.org/'
license=('GPLv3')
depends=('qt5-base' 'pcre')
conflicts=('robomongo')
_tarfile="robo3t-${_pkgver}-linux-x86_64-c93c6b0"
source=("https://download.robomongo.org/${_pkgver}/linux/${_tarfile}.tar.gz"
        'https://raw.githubusercontent.com/paralect/robomongo/master/src/robomongo/gui/resources/icons/logo.png'
        'robomongo.desktop')
sha256sums=('fa977cb21c9d1c53fe8ca3323a06b044623fc722116b25dbdd889db701b20c90'
            '62afd8e83603f0785b21ec8692f6945438e00faf068e35dd9c00986e46419196'
            '33f5ce47f5883733db48ea80e88c404e585ccbcf387c40b1a521e44f52e43d9c')

package() {
  install -Dm0755 "$srcdir/${_tarfile}/bin/robo3t" "$pkgdir/usr/bin/robo3t"
  install -Dm0644 "$srcdir/robomongo.desktop" "$pkgdir/usr/share/applications/robomongo.desktop"
  install -Dm0644 "$srcdir/logo.png" "$pkgdir/usr/share/pixmaps/robomongo.png"
  install -Dm0644 "$srcdir/${_tarfile}/LICENSE" "$pkgdir/usr/share/licenses/robomongo/LICENSE"
  install -Dm0644 "$srcdir/${_tarfile}/COPYRIGHT" "$pkgdir/usr/share/doc/robomongo/COPYRIGHT"
}
