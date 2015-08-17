# Maintainer: Hugo Rodrigues <hugorodrigues at openmailbox dot com>

pkgname=toggle-input
pkgver=1.0.0
pkgrel=2
pkgdesc="Enable and disable xorg input devices in a easy and clean way"
arch=('any')
url="https://github.com/Hugao/ToggleInput"
license=('GPL3')
groups=('xorg-apps')
depends=('grep' 'xorg-xinput' 'bash')
makedepends=('git')
conflicts=('toggle-input-git')
source=("git://github.com/Hugao/ToggleInput.git")
md5sums=('SKIP')

prepare() {
	cd $srcdir/ToggleInput/
	git checkout tags/v$pkgver-$pkgrel
}

package() {
	install -Dm755 "$srcdir/ToggleInput/src/toggleinput.sh" "$pkgdir/usr/bin/toggleinput"
}
