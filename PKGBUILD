pkgname=brother-mfcl2700dw
pkgver=3.2.0
pkgrel=1
pkgdesc="LPR/cupswrapper driver for Brother MFC-L2700DW"
arch=(i686 x86_64)
depends=(lib32-glibc perl)
license=(GPL)
source=(http://download.brother.com/welcome/dlf101789/mfcl2700dwlpr-3.2.0-1.i386.rpm
        http://download.brother.com/welcome/dlf101790/mfcl2700dwcupswrapper-3.2.0-1.i386.rpm)
md5sums=(SKIP
         SKIP)

package() {
  cp -r "$srcdir/opt" "$pkgdir"
  mkdir -p "$pkgdir/usr/lib/cups/filter"
  ln -s /opt/brother/Printers/MFCL2700DW/cupswrapper/brother_lpdwrapper_MFCL2700DW "$pkgdir/usr/lib/cups/filter"
  mkdir -p "$pkgdir/usr/share/cups/model"
  ln -s /opt/brother/Printers/MFCL2700DW/cupswrapper/brother-MFCL2700DW-cups-en.ppd "$pkgdir/usr/share/cups/model"
  install -D "$srcdir/opt/brother/Printers/MFCL2700DW/cupswrapper/Copying" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.txt"
}
