# Maintainer: Diego <cdprincipe@at@gmail@dot@com>

pkgname=gtk-theme-numix-git
pkgver=146.d782b3c
pkgrel=1
pkgdesc="A flat and light theme with a modern look that support Openbox, Xfce, Gnome, Unity and KDE"
arch=('any')
url="https://github.com/shimmerproject/Numix"
license=('GPL3')
depends=('gtk-engine-murrine')
makedepends=('git')
optdepends=('qtcurve-style-numix: KDE QtCurve theme in Numix style')
provides=('gtk-theme-numix')
conflicts=('gtk-theme-numix')
source=('git://github.com/shimmerproject/Numix.git')
md5sums=('SKIP')


pkgver() {
  cd Numix
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
#  git describe | sed 's/^v//;s/-/./g;s/_/./g;'
}

package() {
  cd Numix

  # create theme dir
  install -d -m 755 "$pkgdir"/usr/share/themes/Numix

  # clean up
  rm -rf {.git,.gitignore,CREDITS,LICENSE,README}

  # install theme
  cp -r . "$pkgdir"/usr/share/themes/Numix/
}
