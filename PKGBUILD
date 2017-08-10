# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=networkmanager-s6serv
pkgver=0.1
pkgrel=2
pkgdesc="networkmanager service for s6"
arch=(x86_64)
license=('beerware')
depends=('networkmanager' 's6' 's6-rc' 's6-boot')
conflicts=()
install=networkmanager-s6serv.install
source=('networkmanager.daemon.run.s6'
		'networkmanager.log.run.s6'
		'LICENSE')
md5sums=('ec463a5215a9135565812950c731c7c5'
         'f3dd34f71dd7d961cca97d3aab564f6b'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/networkmanager.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/networkmanager/run"
	
	# log
	install -Dm 0755 "$srcdir/networkmanager.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/networkmanager/log/run"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/networkmanager-s6serv/LICENSE"
}
