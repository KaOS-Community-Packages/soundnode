pkgname=soundnode
pkgver=0.6.1
pkgrel=1
pkgdesc="Soundcloud client for the desktop"
arch=('x86_64')
url="http://www.soundnodeapp.com/"
license=('GPL3')

# Required, otherwise it won't run.
options=('!strip')

makedepends=()
depends=()
optdepends=()

# I couldn't figure out how to build it properly and the website has no per-release
# archives. The SHA256sums will fail if it updates; that should be an indication that
# this package has become out of date.
source_x86_64=("http://www.soundnodeapp.com/downloads/linux64/Soundnode-App.zip")

# Generic sources.
source=("https://raw.githubusercontent.com/Soundnode/soundnode-app/0.6.1/app/soundnode.png"
"soundnode-app.desktop")

sha256sums_x86_64=('9cdec26938b3463568f14566f698c619d72c2dff66fc858079df1a89c970527d')

# Generic checksums.
sha256sums=('SKIP')

package() {
        install -d -m 755 ${pkgdir}/opt/
        install -d -m 755 ${pkgdir}/usr/share/applications/


        install -D -m 644 ${srcdir}/soundnode-app.desktop ${pkgdir}/usr/share/applications/

        rm ${srcdir}/Soundnode-App.zip
        rm ${srcdir}/soundnode-app.desktop
	cp -Lr ${srcdir} $pkgdir/opt/${pkgname}
}
