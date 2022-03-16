pkgname=overlayroot
pkgver=0.8
pkgrel=1
pkgdesc="overlayFS root file system"
arch=('any')
url="https://github.com/ugjka/arch-overlayroot"
license=('MIT')
depends=(
  'mkinitcpio'
  'arch-install-scripts'
)
install=overlayroot.install
source=(
  'overlayroot.install'
  'initcpio-install-overlayroot'
  'initcpio-hooks-overlayroot'
  'rwrootfs'
  'fsck.overlay'
  'journald-volatile-storage.conf'
  'overlayroot-motd.sh'
  'flush.service'
  'flush_overlay'
)
sha256sums=(
  'SKIP'
  'SKIP'
  'SKIP'
  'SKIP'
  'SKIP'
  'SKIP'
  'SKIP'
  'SKIP'
  'SKIP'
)

build() {
  :
}

package() {
  install -Dm644 "$srcdir/initcpio-install-overlayroot" "$pkgdir/usr/lib/initcpio/install/overlayroot"
  install -Dm644 "$srcdir/initcpio-hooks-overlayroot" "$pkgdir/usr/lib/initcpio/hooks/overlayroot"
  install -Dm644 "$srcdir/journald-volatile-storage.conf" "$pkgdir/usr/lib/systemd/journald.conf.d/volatile-storage.conf"
  install -Dm755 "$srcdir/rwrootfs" "$pkgdir/usr/bin/rwrootfs"
  install -Dm755 "$srcdir/fsck.overlay" "$pkgdir/usr/bin/fsck.overlay"
  install -Dm644 "$srcdir/overlayroot-motd.sh" "$pkgdir/etc/profile.d/overlayroot-motd.sh"
  install -Dm644 "$srcdir/flush.service" "$pkgdir/usr/lib/systemd/system/flush.service"
  install -Dm755 "$srcdir/flush_overlay" "$pkgdir/usr/bin/flush_overlay"
}
