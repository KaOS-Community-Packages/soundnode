pkgname=soundnode
pkgver=0.6.2
pkgrel=1
pkgdesc="Soundcloud client for the desktop"
arch=('x86_64')
url="http://www.soundnodeapp.com/"
license=('GPL3')
depends=('gconf')
source=("http://www.soundnodeapp.com/downloads/linux64/Soundnode-App.zip"
        "https://raw.githubusercontent.com/Soundnode/soundnode-app/0.6.2/app/soundnode.png"
        "soundnode-app.desktop")
sha256sums=('e3d6b88150d286645553f803edd6163e53e967415fa9e38d7bbbf9f9182f7a7a'
            'aaae33882ab1e2334b4a33b4235cbdd4beb1379b08f5fa3a0a270f716ea43fa7'
            'd4b4e8825ab3770d93358d6dd7aefbbabcfccf51392535fdb3fb640c962b78e6')

package() {
        install -d -m 755 ${pkgdir}/opt/
        install -d -m 755 ${pkgdir}/usr/share/applications/
        install -D -m 644 ${srcdir}/soundnode-app.desktop ${pkgdir}/usr/share/applications/
        rm ${srcdir}/Soundnode-App.zip
        rm ${srcdir}/soundnode-app.desktop
        cp -Lr ${srcdir} $pkgdir/opt/${pkgname}
}
