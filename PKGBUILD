#Maintainer: Jose C.

pkgname=android-studio
pkgver='2020.3.1.26'
pkgrel=1
pkgdesc='Provides the fastest tools for building apps on every type of Android device'
arch=('i686' 'x86_64')
options=('!strip')
url='https://developer.android.com/studio'
license=('Commercial')
provides=('android-studio')
conflicts=('android-studio')

_filename='android-studio-${pkgver}-linux.tar.gz'
_filextract='android-studio'

source=("https://dl.google.com/dl/android/studio/ide-zips/$pkgver/android-studio-$pkgver-linux.tar.gz"
  "${pkgname}.desktop")

sha256sums=('344d858235ed5d3095ac25916a4a8f8730069f76e5a5fd0eba02522af88f541b'
  'ea739f5bfa52e89915965081233c600fe316fbf859b474784afa75a2dbb9948e')

package() {
  #Create directorires with permission rwxr-xr-x
  install -m755 -d "${pkgdir}/usr/share" "${pkgdir}/usr/bin" "${pkgdir}/usr/share/applications"
  
  #Copy files to pkg destination
  cp -r "${srcdir}/${_filextract}" "${pkgdir}/usr/share/${pkgname}"
  chown -R root:root "${pkgdir}/usr/share/${pkgname}"

  ln -s "/usr/share/${pkgname}/bin/studio.sh" "${pkgdir}/usr/bin/studio"
  install -m644 "${srcdir}/${pkgname}.desktop" "${pkgdir}/usr/share/applications"
}
