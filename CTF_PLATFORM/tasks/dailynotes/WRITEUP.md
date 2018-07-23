# Dailynotes: Write-up

Перед нами — супер-сайт с заметками. По заверениям разработчиков, все заметки зашифрованы [ROT0](https://ru.wikipedia.org/wiki/ROT13) и им пользуется сам God!

Регистрируемся на главной странице и попадаем в личный кабинет.

В личном кабинете всё просто — заметки и настройки.

Замечаем две странных и непривычных вещи:

* в настройках для смены пароля не нужно вводить старый пароль
* страница настроек имеет вид `/profile/123/settings/`

Убеждаемся, что 123 — наш ID пользователя. Удовлетворим наше любопытство и перейдем по ссылке `/profile/1/settings`.

Вау, открывается! Меняем пароль… и снова успех! Входим под нашим пользователем и новым паролем — поменялся **не наш** пароль. Наверное, мы смогли поменять пароль пользователя с ID = 1. Заходим на `/profile/1/` и видим, что это пользователь `god`.

Заходим на сайт с логином `god` и новым паролем и получаем флаг в одной из заметок.

Флаг: **ugra_very_very_dirty_web**