pkgname=soundnode
pkgver=0.6.5
pkgrel=1
pkgdesc="Soundcloud client for the desktop"
arch=('x86_64')
url="http://www.soundnodeapp.com/"
license=('GPL3')
depends=('gconf' 'gtk2' 'libxtst' 'nss' 'alsa-lib' 'libnotify' 'fontconfig')
source=("http://www.soundnodeapp.com/downloads/linux64/Soundnode.zip"
        "https://raw.githubusercontent.com/Soundnode/soundnode-app/0.6.2/app/soundnode.png"
        "soundnode-app.desktop")
options=("!strip")
sha256sums=('ecf085044347a4b35ea4c558ab65296edd8c107f84f88fb5e88e5b72454475c1'
            'aaae33882ab1e2334b4a33b4235cbdd4beb1379b08f5fa3a0a270f716ea43fa7'
            '3ef95758b2eb2e85b8666b48786f4f7f440fcc9efd170efcff9aec84e79f0427')

package() {
        install -d -m 755 $pkgdir/opt/
        cp -Lr $srcdir $pkgdir/opt/$pkgname
        install -dm755 $pkgdir/usr/bin
        ln -s /opt/soundnode/Soundnode $pkgdir/usr/bin/soundnode
        install -dm755 $pkgdir/usr/share/applications/
        install -Dm644 "$srcdir"/soundnode-app.desktop "$pkgdir"/usr/share/applications/
        ## the size could be wrong but still should be fine like this
        install -d -m 755 "$pkgdir"/usr/share/icons/hicolor/32x32/apps
        ln -s  /opt/$pkgname/$pkgname.png   $pkgdir/usr/share/icons/hicolor/32x32/apps/$pkgname.png

        rm $pkgdir/opt/$pkgname/{soundnode-app.desktop,Soundnode.zip}
        }
