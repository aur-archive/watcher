
pkgname=watcher
pkgver=1.2
pkgrel=3
pkgdesc="Watcher, a Recursive incron Alternative"
arch=(any)
url="https://github.com/splitbrain/Watcher"
license=('MIT')
depends=('python2' 'python2-pyinotify' 'python2-systemd')
backup=('etc/conf.d/watcher.ini')
source=('LICENSE'
	'README'
	'watcher.ini'
	'watcher.py'
	'watcher.service')
md5sums=('7a70dca39cec6eaaf33f7815df4fd21f'
	'cbceefe3f60ee173ea5976a4149324c0'
	'41d30fea52da5ebae58b81cb74cf03fb'
	'9a0eb7dd47a1526ab4ef1248ebb31321'
	'7a4b0e5c9df1f1ca15e29b7648217703')

package() {
	cd "${srcdir}"
	install -Dm 644 "watcher.ini" "${pkgdir}/etc/conf.d/watcher.ini"
	install -Dm 644 "watcher.service" "${pkgdir}/usr/lib/systemd/system/watcher.service"
	install -Dm 644 "LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSES"
	install -Dm 755 "watcher.py" "${pkgdir}/usr/share/${pkgname}/watcher.py"
	install -Dm 644 "README" "${pkgdir}/usr/share/doc/${pkgname}/README"
}
