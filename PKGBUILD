# Maintainer: miaoermua <miaoermua@gmail.com>

pkgname=fnpack-bin
pkgver=1.2.0
pkgrel=1
pkgdesc="飞牛 fnOS 应用打包工具"
arch=('x86_64' 'aarch64')
url="https://developer.fnnas.com/docs/cli/fnpack"
license=('custom')
provides=('fnpack')
conflicts=('fnpack')

case "$CARCH" in
  x86_64)
    _arch=amd64
    source=("https://static2.fnnas.com/fnpack/fnpack-${pkgver}-linux-amd64")
    sha256sums=('SKIP')
    ;;
  aarch64)
    _arch=arm64
    source=("https://static2.fnnas.com/fnpack/fnpack-${pkgver}-linux-arm64")
    sha256sums=('SKIP')
    ;;
  *)
    error "Unsupported architecture: $CARCH"
    exit 1
    ;;
esac

package() {
  install -Dm755 "${srcdir}/fnpack-${pkgver}-linux-${_arch}" "${pkgdir}/usr/bin/fnpack"
}