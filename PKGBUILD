# Maintainer: Sri Hari Haran T <heodev@proton.me>
pkgname=justfetch
pkgver=0.1.0
pkgrel=1
pkgdesc="A Bash-based Linux system information tool with ASCII art"
arch=('any')
url="https://github.com/SriHariHaran-T/justfetch"
license=('MIT')
depends=('bash' 'systemd' 'procps-ng' 'coreutils' 'gawk' 'lshw' 'pciutils')
optdepends=('ascii-image-converter: convert custom images into ASCII logos')
source=("$pkgname-$pkgver.tar.gz::https://github.com/SriHariHaran-T/justfetch/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('13a89973272480147b891e11885f9601c232362a7fbde694d9f87bc43afadff0')

package() {
    cd "$srcdir/JustFetch-$pkgver"

    install -d "$pkgdir/usr/lib/justfetch"
    install -d "$pkgdir/usr/bin"

    install -m755 justfetch "$pkgdir/usr/lib/justfetch/justfetch"
    install -m755 information "$pkgdir/usr/lib/justfetch/information"
    install -m755 logo "$pkgdir/usr/lib/justfetch/logo"

    cp -r logos "$pkgdir/usr/lib/justfetch/"
    cp -r assets "$pkgdir/usr/lib/justfetch/"
    install -m644 LICENSE "$pkgdir/usr/lib/justfetch/LICENSE"
    install -m644 README.md "$pkgdir/usr/lib/justfetch/README.md"

    ln -s /usr/lib/justfetch/justfetch "$pkgdir/usr/bin/justfetch"
}
