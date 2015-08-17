# Maintainer: James Bulmer <nekinie@gmail.com>

pkgname="python2-glanceclient-deb"
pkgver=0.12.0
pkgrel=1
pkgdesc="Client library for Openstack image"
arch=("i686" "x86_64")
url="http://docs.openstack.org/developer/python-glanceclient/"
license=("Apache")

depends=(
  "python2"
  "python2-pbr"
  "python2-keystoneclient-deb"
  "python2-pyopenssl"
  "python2-prettytable"
  "python2-warlock"
)

makedepends=("python2-setuptools")
conflicts=("python2-glanceclient" "python2-glanceclient-git")
source=("http://archive.ubuntu.com/ubuntu/pool/main/p/python-glanceclient/python-glanceclient_${pkgver}.orig.tar.gz")
md5sums=("8eddc27a90121c3d2ca6f6141de30f0d")

build() {
  cd "${srcdir}/python-glanceclient-${pkgver}/"
  python2 setup.py build
}

package() {
  cd "${srcdir}/python-glanceclient-${pkgver}/"
  python2 setup.py install --root="${pkgdir}/" --optimize=1
}