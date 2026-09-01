pkgname=elogind-usersv-backend-s6
pkgver=0.1.0
pkgrel=1
pkgdesc='Native per-user s6 backend for elogind-usersv on Artix'
arch=('any')
url='https://github.com/username13121/elogind-usersv-s6-artix'
license=('GPL-3.0-only')
depends=('elogind-usersv' 's6' 's6-rc')
source=('s6' 'LICENSE')
sha256sums=('40c7f33b04da4c2472190b9460f69668191ac395e9ece6e1c231e08ad91e6cef'
            'fb981668c18a279e285fc4d83fba1e836cc84dd4daa73c9697d3cfd2d8aca6e0')

package() {
    install -Dm755 s6 "$pkgdir/usr/libexec/elogind-usersv/backends/s6"
    install -dm755 \
        "$pkgdir/etc/s6/user/sv" \
        "$pkgdir/etc/s6/user/adminsv"
    install -Dm644 LICENSE \
        "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
