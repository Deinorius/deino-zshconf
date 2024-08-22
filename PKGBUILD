# Maintainer: Chrysostomus @forum.manjaro.org
# Developer: pheiduck @forum.manjaro.org

pkgname=manjaro-zsh-config
pkgver=0.25
pkgrel=3
pkgdesc="Zsh configuration loosely based on manjaro for my Arch install"
arch=(any)
url="https://github.com/Deinorius/$pkgname"
_gitcommit=e19c7c5e902a3085f918fb1fc6d0c1fd43c559c8
license=('MIT')
conflicts=('grml-zsh-config')
depends=('zsh-autosuggestions'
	'zsh-syntax-highlighting'
	'zsh-completions'
	'zsh-history-substring-search'
	'zsh'
	'pkgfile'
	'nerd-fonts-noto-sans-mono'
	'zsh-theme-powerlevel10k')
backup=(root/.zshrc)
source=("$pkgname.tar.gz::$url/archive/$_gitcommit.tar.gz")
sha256sums=('SKIP')

package() {
	cd ${srcdir}
	install -D -m644 $srcdir/$pkgname-$_gitcommit/.zshrc ${pkgdir}/etc/skel/.zshrc
	install -D -m644 $srcdir/$pkgname-$_gitcommit/manjaro-zsh-config ${pkgdir}/usr/share/zsh/manjaro-zsh-config
	install -D -m644 $srcdir/$pkgname-$_gitcommit/manjaro-zsh-prompt ${pkgdir}/usr/share/zsh/manjaro-zsh-prompt
	install -D -m644 $srcdir/$pkgname-$_gitcommit/zsh-maia-prompt ${pkgdir}/usr/share/zsh/zsh-maia-prompt
	install -D -m644 $srcdir/$pkgname-$_gitcommit/p10k.zsh ${pkgdir}/usr/share/zsh/p10k.zsh
	install -D -m644 $srcdir/$pkgname-$_gitcommit/p10k.zsh ${pkgdir}/usr/share/zsh/p10k-portable.zsh
	mkdir -p $pkgdir/usr/share/zsh/scripts
	cp -r $srcdir/$pkgname-$_gitcommit/base16-shell $pkgdir/usr/share/zsh/scripts
	chmod a+x $pkgdir/usr/share/zsh/scripts/base16-shell/*
}
