# Contributor: Emiliano Vavassori <syntaxerrormmm(at)gmail.com>
# Maintainer: nbryskin
pkgname=ruby-heroku-api
_gemname=heroku-api
pkgver=0.3.23
pkgrel=1
pkgdesc="Ruby Client for the Heroku API"
arch=('any')
url="http://github.com/heroku/heroku.rb"
license=('MIT')
depends=('ruby' 'ruby-excon>=0.44' 'ruby-multi_json>=1.8')
makedepends=('rubygems')
source=(http://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
md5sums=('8cea3246bd776670205ffbe5e5ef2c19')

package() {
  cd "${srcdir}"
  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"

  gem install --ignore-dependencies --no-user-install -i "${pkgdir}${_gemdir}" "${_gemname}-${pkgver}.gem"
}
