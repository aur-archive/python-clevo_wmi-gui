# Maintainer: Your Name <youremail@domain.com>
pkgname=python-clevo_wmi-gui
pkgver=7.674ae23
pkgrel=1
pkgdesc="GUI for Clevo Notebooks with a backlit keyboard with controllable LEDs."
arch=("x86_64" "i686")
url="https://github.com/ChristophHaag/clevo_wmi_kivy-gui"
license=('GPL')
depends=('python3' 'python3-kivy-git' 'clevo_wmi') #should work with python2 too
options=('!emptydirs')
source=("git+https://github.com/ChristophHaag/clevo_wmi_kivy-gui.git"
        "clevo_wmi-gui.sh")

package() {
  cd "$srcdir/clevo_wmi_kivy-gui"
  python setup.py install --root="$pkgdir/" --optimize=1
  install -d "$pkgdir/usr/bin"
  install -m755 "$srcdir/clevo_wmi-gui.sh" "$pkgdir/usr/bin/clevo_wmi-gui"
}

pkgver() {
  cd "$srcdir/clevo_wmi_kivy-gui"
  echo $(git rev-list --count HEAD).$(git rev-parse --short HEAD)
}
md5sums=('SKIP'
         '831350cbf86cf21c0c82d0f3c03c059c')
