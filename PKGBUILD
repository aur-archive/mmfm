pkgname=mmfm
pkgver=20121111
pkgrel=2
pkgdesc="An Internet-Radio toolkit(P.R.China)"
url="http://wiki.linuxdeepin.com/index.php/MM%E7%94%B5%E5%8F%B0"
license="unknow"
arch=('any')
provides=('mmfm')
depends=('python2'  'pywebkitgtk' 'pygtk' 'python2-notify' 'gst-plugins-base-libs')
source=('http://erhandsome.org/php/files/mmfm.tar.lzma')
md5sums=('f67a45e40908aa9cf7e9d7c823678163')
build()
{
cd "${srcdir}"
rm readme wlist mmfm.tar.lzma
mkdir -p usr/bin
mv run_me usr/bin/mmfm
mkdir -p usr/share/applications
mv bin usr/share/mmfm
#===
cat << EOF > usr/share/applications/mmfm.desktop
[Desktop Entry]
Encoding=UTF-8
Name=MM电台
Comment=使用网络电台
Icon=music
Exec=mmfm
Terminal=false
Type=AudioVideo;Audio;
Categories=AudioVideo;Audio;
EOF
#===
chmod -R 755 usr/share
chmod -R 644 usr/share/mmfm/pics
chmod 755 usr/share/mmfm/pics
chmod 644 usr/share/applications/mmfm.desktop
chmod -R 755 usr/bin
}
package()
{
    cp "$srcdir"/* "${pkgdir}" -rPp
}
