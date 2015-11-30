pkgname=texlive-pscyr
pkgver=0.4d
pkgrel=1
license=('GPL')
depends=('texlive-core' 'texlive-latexextra' 'texlive-langcyrillic')
pkgdesc='A LaTeX package with nice cyrillic fonts'
url='none'
arch=('any')
install=texlive-pscyr.install
source=("https://github.com/AndreyAkinshin/Russian-Phd-LaTeX-Dissertation-Template/blob/master/PSCyr/pscyr$pkgver.zip?raw=true")
sha256sums=('4ed44287c45022337c95f43f7b94212b4ff87feee21870327a7220099a8988bf')

package() {
          # tweak from https://gist.github.com/tonkonogov/79844f9276da94810163
	  mkdir -p pscyr/fonts/map pscyr/fonts/enc
	  cp pscyr/dvips/pscyr/*.map pscyr/fonts/map/
	  cp pscyr/dvips/pscyr/*.enc pscyr/fonts/enc/
	  # end tweak
	  target=`kpsewhich -expand-var='$TEXMFMAIN'`
          dir=$pkgdir$target
	  mkdir -p $pkgdir$target
	  cp -r pscyr/* $dir/
	  echo "fadr6t   AdvertisementPSCyr \"T2AEncoding ReEncodeFont\" <t2a.enc <adver4.pfb" >> $dir/fonts/map/pscyr.map

    }

