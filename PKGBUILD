# Maintainer: Peter Lewis <plewis@aur.archlinux.org>

pkgname=perl-data-amf-packet
pkgver=0.09
pkgrel=1
pkgdesc="CPAN package Data::AMF::Packet"
arch=('any')
url="http://search.cpan.org/~typester/Data-AMF-0.09/"
license=('GPL' 'PerlArtistic')
source=('http://search.cpan.org/CPAN/authors/id/T/TY/TYPESTER/Data-AMF-0.09.tar.gz')
options=(!emptydirs)
sha256sums=('a9121dc7d88c38986c9a794994acfb67cb5d2dea70140299ebfb4f468ed37898')

build() {
  cd $srcdir/Data-AMF-${pkgver}

  PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor
  make
}

package() {
  cd $srcdir/Data-AMF-${pkgver}
  make install DESTDIR="${pkgdir}"

  # remove perllocal.pod and .packlist
  find ${pkgdir} -name perllocal.pod -delete
  find ${pkgdir} -name .packlist -delete
}

# vim:set ts=2 sw=2 et:

