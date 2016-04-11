pkgname=soundnode
pkgver=0.6.4
pkgrel=1
pkgdesc="Soundcloud client for the desktop"
arch=('x86_64')
url="http://www.soundnodeapp.com/"
license=('GPL3')
depends=('gconf' 'gtk2' 'libxtst' 'nss' 'alsa-lib' 'libnotify' 'fontconfig')
options=('!strip')
source=("http://www.soundnodeapp.com/downloads/linux64/Soundnode-App.zip"
        "https://raw.githubusercontent.com/Soundnode/soundnode-app/0.6.4/app/soundnode.png"
        "soundnode-app.desktop")
options=("!strip")
sha256sums=('2b0dbdb6a59546472f9621b25be1b29aa60c22c3f8e692940dad698de85aa432'
            'aaae33882ab1e2334b4a33b4235cbdd4beb1379b08f5fa3a0a270f716ea43fa7'
            '3ef95758b2eb2e85b8666b48786f4f7f440fcc9efd170efcff9aec84e79f0427')

package() {
        install -d -m 755 $pkgdir/opt/
        cp -Lr $srcdir $pkgdir/opt/$pkgname
        install -dm755 $pkgdir/usr/bin
        ln -s /opt/soundnode/Soundnode $pkgdir/usr/bin/soundnode
        install -dm755 $pkgdir/usr/share/applications/
        install -Dm644 "$srcdir"/soundnode-app.desktop "$pkgdir"/usr/share/applications/
        install -d -m 755 $pkgdir/usr/share/pixmaps
        ln -s  /opt/$pkgname/$pkgname.png   $pkgdir/usr/share/pixmaps/$pkgname.png

        rm $pkgdir/opt/$pkgname/{soundnode-app.desktop,Soundnode-App.zip}
        }
