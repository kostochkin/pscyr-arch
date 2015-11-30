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
	  dir=$pkgdir/usr/share/texmf-dist
	  mkdir -p $dir
	  cp -r pscyr/tex pscyr/doc pscyr/dvipdfm pscyr/dvips pscyr/fonts $dir/
    }

