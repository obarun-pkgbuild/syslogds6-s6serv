# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=syslogds6-s6serv
pkgver=0.2
pkgrel=3
pkgdesc="syslogds6 service for s6"
arch=(x86_64)
license=('beerware')
depends=('s6' 's6-rc' 's6-boot')
conflicts=()
source=('syslogds6.daemon.notification-fd.s6'
		'syslogds6.daemon.run.s6'
		'syslogds6.log.run.s6'
		'syslogds6.logd'
		'LOGSCRIPT'
		'LICENSE')
md5sums=('6d7fce9fee471194aa8b5b6e47267f03'
         '31850f8af447c1e8dfde19148d48ba7b'
         'f8dfc30b826c5e649b69e76211ddcd8a'
         '1b28c51cbce332a27350e91e03fd0596'
         '4589d7ee683bf01ae8dedcdcc12a5eac'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/syslogds6.daemon.notification-fd.s6" "$pkgdir/etc/s6-serv/available/classic/syslogds6/notification-fd"
	install -Dm 0755 "$srcdir/syslogds6.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/syslogds6/run"
	
	# log
	install -Dm 0755 "$srcdir/syslogds6.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/syslogds6/log/run"
	install -Dm 0755 "$srcdir/LOGSCRIPT" "$pkgdir/etc/s6-serv/available/classic/syslogds6/log/env/LOGSCRIPT"
	install -Dm 0644 "$srcdir/syslogds6.logd" "$pkgdir/etc/s6-serv/log.d/syslogds6"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/syslogds6-s6serv/LICENSE"
}
