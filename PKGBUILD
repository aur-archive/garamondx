pkgname=garamondx
pkgver=1.096
pkgrel=1
pkgdesc="‘Expert’-like extensions to URW Garamond, and math italic (for texlive in conjunction with urw-garamond package)."
arch=('any')
license=('custom')
url=("http://www.ctan.org/tex-archive/fonts/garamondx")
depends=('urw-garamond' 'texlive-core')
install=$pkgname.install
source=(http://mirrors.ctan.org/fonts/garamondx.zip garamondx.maps)
md5sums=('a977464346897ab880e53f813a6b6294'
         '80761a71120a9861400927b591ac463f')

package() {
  cd $srcdir
  _texmf_root=usr/share/texmf
  install -d -m755 "$pkgdir/var/lib/texmf/arch/installedpkgs"
  install -m644 "$pkgname.maps" "$pkgdir/var/lib/texmf/arch/installedpkgs"

  install -d -m755 "$pkgdir/$_texmf_root/fonts/afm/urw/garamond"
  install -m644 $pkgname/afm/*.afm "$pkgdir/$_texmf_root/fonts/afm/urw/garamond"

  install -d -m755 "$pkgdir/$_texmf_root/fonts/enc"
  install -m644 $pkgname/enc/*.enc "$pkgdir/$_texmf_root/fonts/enc"

  install -d -m755 "$pkgdir/$_texmf_root/fonts/map/dvips/zgm"
  install -m644 $pkgname/map/*.map "$pkgdir/$_texmf_root/fonts/map/dvips/zgm"

  install -d -m755 "$pkgdir/$_texmf_root/tex"
  install -m644 $pkgname/tex/* "$pkgdir/$_texmf_root/tex"

  install -d -m755 "$pkgdir/$_texmf_root/fonts/tfm/urw/garamond"
  install -m644 $pkgname/tfm/*.tfm "$pkgdir/$_texmf_root/fonts/tfm/urw/garamond"

  install -d -m755 "$pkgdir/$_texmf_root/fonts/type1/urw/garamond"
  install -m644 $pkgname/type1/*.pfb "$pkgdir/$_texmf_root/fonts/type1/urw/garamond"

  install -d -m755 "$pkgdir/$_texmf_root/fonts/vf/urw/garamond"
  install -m644 $pkgname/vf/*.vf "$pkgdir/$_texmf_root/fonts/vf/urw/garamond"

  install -Dm755 $pkgname/README $pkgdir/usr/share/licenses/$pkgname/README
}
