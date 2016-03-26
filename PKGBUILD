pkgname=soundnode
pkgver=0.6.3
pkgrel=1
pkgdesc="Soundcloud client for the desktop"
arch=('x86_64')
url="http://www.soundnodeapp.com/"
license=('GPL3')
depends=('gconf' 'gtk2')
options=('!strip')
source=("http://www.soundnodeapp.com/downloads/linux64/Soundnode-App.zip"
        "https://raw.githubusercontent.com/Soundnode/soundnode-app/0.6.2/app/soundnode.png"
        "soundnode-app.desktop")
sha256sums=('15aa9524e37fc52276e4ec19a22936352785f8c132ead8b59c7bf6cdff0b1442'
            'aaae33882ab1e2334b4a33b4235cbdd4beb1379b08f5fa3a0a270f716ea43fa7'
            '3ef95758b2eb2e85b8666b48786f4f7f440fcc9efd170efcff9aec84e79f0427')
noextract=('Soundnode-App.zip')
prepare() {
        mkdir ${srcdir}/opt
        bsdtar -xf Soundnode-App.zip -C ${srcdir}/opt
}
package() {

        install -d -m 755 "$pkgdir"/opt/
        cp -r "$srcdir"/opt "$pkgdir"/opt/"$pkgname"
        install -dm755 "$pkgdir"/usr/bin
        ln -s /opt/soundnode/Soundnode "$pkgdir"/usr/bin/soundnode
        install -dm755 "$pkgdir"/usr/share/applications/
        install -m644 ${srcdir}/soundnode-app.desktop ${pkgdir}/usr/share/applications/
        cp soundnode.png $pkgdir/opt/${pkgname}
}
