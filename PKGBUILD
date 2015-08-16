# Contributor: Tilo Brueckner  blueperil at gmx de

pkgname=krunner-firefoxbookmarks
pkgver=0.2.2
pkgrel=1
pkgdesc='A runner that integrates mozilla firefox bookmarks into krunner'
arch=('i686' 'x86_64')
url=(http://kde-apps.org/content/show.php/Browse+Firefox+Bookmarks?content=141042)
license=('GPL')
depends=('kdebase-workspace' 'firefox')
makedepends=('automoc4' 'cmake')
source=('http://opendesktop.org/CONTENT/content-files/141042-browsefirefoxbookmarks.tar.bz2')
md5sums=('c9f9155c92772c91dafd58888d637cd7')

build() {
  cd ${srcdir}/plasma-runner-browsefirefoxbookmarks/

  mkdir build
  cd build
  cmake ../ -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` || return 1
  make || return 1
}

package() {
  cd ${srcdir}/plasma-runner-browsefirefoxbookmarks/build

  make DESTDIR=$pkgdir install || return 1
}
