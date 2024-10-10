# Maintainer: Naomi Calabretta <nyaomicalabretta at gmail dot com>

pkgname=plymouth-openrc-plugin
pkgver=0.3.0
pkgrel=1
pkgdesc='Plymouth plugin for OpenRC'
arch=('x86_64' 'i686' 'armv7h' 'aarch64')
url='https://github.com/Kangie/plymouth-openrc-plugin'
license=('GPL2')
makedepends=('meson' 'ninja')
depends=('plymouth' 'openrc')
source=('https://github.com/Kangie/plymouth-openrc-plugin/archive/refs/tags/v0.3.0.tar.gz')
sha256sums=('a63ed703eab8be816a754c2965324619ddcb21cce6bd13405e459ec663e22e5c')

build() {
	cd "$srcdir/$pkgname-$pkgver"
	artix-meson build
	ninja -C build
}

package() {
	cd "$srcdir/$pkgname-$pkgver"
	DESTDIR="$pkgdir" ninja install -C build
}
