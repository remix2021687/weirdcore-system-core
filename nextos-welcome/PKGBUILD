pkgname=os-welcome
pkgver=1.0.0
pkgrel=1
pkgdesc="Скрипт приветствия для NextOS"
arch=('any')
license=('MIT')
depends=('bash zsh')

package() {
    # Создаем системную папку для исполняемых файлов внутри будущего пакета
    install -Dm755 "${srcdir}/../welcome.sh" "${pkgdir}/usr/local/bin/nextos-welcome"

    # Добавляем наш скрипт в автозапуск терминала для всех пользователей
    mkdir -p "${pkgdir}/etc/profile.d"
    echo "/usr/local/bin/nextos-welcome" > "${pkgdir}/etc/profile.d/nextos-welcome.sh"
}