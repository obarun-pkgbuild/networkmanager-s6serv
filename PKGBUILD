# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=networkmanager-s6serv
pkgver=0.1
pkgrel=3
pkgdesc="networkmanager service for s6"
arch=(x86_64)
license=('beerware')
depends=('networkmanager' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('networkmanager.daemon.run.s6'
		'networkmanager.log.run.s6'
		'networkmanager.logd'
		'LICENSE')
md5sums=('ec463a5215a9135565812950c731c7c5'
         'f3dd34f71dd7d961cca97d3aab564f6b'
         '0a27fa272ed28153f878e2bfbc706b19'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/networkmanager.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/networkmanager/run"
	
	# log
	install -Dm 0755 "$srcdir/networkmanager.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/networkmanager/log/run"
	install -Dm 0644 "$srcdir/networkmanager.logd" "$pkgdir/etc/s6-serv/log.d/networkmanager"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/networkmanager-s6serv/LICENSE"
}
