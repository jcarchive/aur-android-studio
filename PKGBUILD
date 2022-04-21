#Maintainer: Jose C.

pkgname=android-studio
pkgver='2021.1.1.23'
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

sha256sums=('b37506cd8ac7a80fe30cd1724e3be5c2d970a7aa6aa3fc9ca745afe3700aabcf'
  '10ca7decc8fda704b2434639ea22ec93cf2baefa4dc7c24902f740fb795235c4')

package() {
  #Create directorires with permission rwxr-xr-x
  install -m755 -d "${pkgdir}/usr/share" "${pkgdir}/usr/bin" "${pkgdir}/usr/share/applications"
  
  #Copy files to pkg destination
  cp -r "${srcdir}/${_filextract}" "${pkgdir}/usr/share/${pkgname}"
  chown -R root:root "${pkgdir}/usr/share/${pkgname}"

  ln -s "/usr/share/${pkgname}/bin/studio.sh" "${pkgdir}/usr/bin/studio"
  install -m644 "${srcdir}/${pkgname}.desktop" "${pkgdir}/usr/share/applications"
}
