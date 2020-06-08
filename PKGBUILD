pkgname=diff-so-fancy
pkgver=1.3.0
pkgrel=1
arch=('x86_64')
pkgdesc='Make your diffs human readable instead of machine readable'
url='https://github.com/so-fancy/diff-so-fancy'
license=('custom:MIT')
depends=('perl')
source=("https://github.com/so-fancy/${pkgname}/archive/v${pkgver}.tar.gz")
sha1sums=('9590b1891a31997d8eec555a813217e80a84a34c')

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  sed -i 's|^use lib .*$|use lib "/usr/share/diff-so-fancy";|' diff-so-fancy
  install -Dm755 "diff-so-fancy" "$pkgdir/usr/bin/diff-so-fancy"
  install -Dm755 "lib/DiffHighlight.pm" "$pkgdir/usr/share/diff-so-fancy/DiffHighlight.pm"
  install -Dm644 "LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
