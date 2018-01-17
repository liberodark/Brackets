# Maintainer: liberodark

pkgname=brackets
pkgver=1.12
pkgrel=1
pkgdesc="An open source code editor for the web"
arch=('x86_64')
url="http://brackets.io/"
license=('MIT')
depends=('xdg-utils')
source_x86_64=("https://github.com/adobe/brackets/releases/download/release-1.12-prerelease/Brackets.Pre-Release-1.12.64-bit.deb")
source=($pkgname.desktop
        $pkgname.svg)
sha512sums=('05c29610362cf28951dd1c1c240cc1f2a44a009816a2b7df6ac1b54cccdc7d3b37c8a68b637ec72d8411019c5532b21c53f198fda7e5f3a8f9081a9f7bbb602e'
         '3eb7212e1343dec8a66a7393cb90b075eff0ca31ddb67066b487b644f2d60dc2a1e855aa5a28dab295b114235f15ed118dd6161cf337e4d28f61bf4ebf7f0628')
sha512sums_x86_64=('9432f7ba5991ae12d790d329d451224aa13f42dd0596efbb62e673491e7b05f92cee0aa24e7fb7b277c471f7f3ce5cf2f6e18a8b57d0565fc40f1fc525a6867c')
        
package() {
  cd $srcdir
  tar xvf data.tar.xz
  cp -r opt $pkgdir
  #suid sandbox
  chmod 4755 "${pkgdir}/opt/brackets/chrome-sandbox"
  install -vDm644 $srcdir/$pkgname.desktop $pkgdir/usr/share/applications/$pkgname.desktop
  install -vDm644 $srcdir/$pkgname.svg $pkgdir/usr/share/pixmaps/$pkgname.svg
}
