# qutiny

# 😐 | Что за чудо-юдо?

`qutiny` — это мульти-форковое ядро базирующееся на основе <a href="https://hub.spigotmc.org/stash/projects/SPIGOT/repos/bukkit/browse">bukkit</a> как и все другие популярные замены <a href="https://github.com/PaperMC/Paper/tree/ver/1.16.5">paper</a>. 🙂

# 🧑 |  Как писали рыбу?

Для написания ядра использовалась обычная система патчей разработанная от [PaperMC](https://papermc.io) по версии [1.16.4/5](https://www.minecraft.net/en-us/article/minecraft-java-edition-1-16-5) ([protocol](https://minecraft.wiki/w/Protocol_version): 754).

# 📂 | Когось форкали?

Для кодовой базы было взято потно нафорканое ядро ластецкой версии от разработчика [foss](https://builtbybit.com/members/foss.211252/) о котором в румайне не знают, но на деле он является автором [SSSpigot](https://builtbybit.com/resources/ssspigot2.14122/), которое активно используют под 1.16.5 сервера в румк.

> [!NOTE]
> Разработчики сборок на эту версию игры обычно забывают про покупку ядра (ой, деняк нет совсем 🤡), поэтому качают с форумов слитые ресурсы, следовательно, не используют актуальную последнюю официальную версию, где есть много исправлений и корректировок.  
> В версиях от 2021 года имеются критические дюпы и уязвимости. 😅

# 🍝 | Откуда пиздили код?

Интерес к SS'у пал когда на данную версию майна у меня не осталось ядер выполняющих необходимые мне задачи, а последние изменения в ядро **SSSpigot** вносились не народным способом (не патчами) 🥺, поэтому необходимо было создать все предыдущие изменения с различных проектов и заказов воедино. 🧐

Такие изменения были у меня в ядрах линейки `bukkit-base` 🎲 (да-да, не оригинальное название), речь о `bukkit-limbo` и `bukkit-game` 🥴 предназначенных уже на [1.18.2](https://www.minecraft.net/en-us/article/minecraft-java-edition-1-18-2), но имеющих схожий функционал.

# 📋 | Чё меняли?

К сожалению, список изменений не был грамотно выверен 😭 и преобразован на читабельный формат, поэтому сызволю расписать краткий пересказ путешествий по этакому коду.

Собсна:
- базовые конфигурации от Vanilla вырезаны;
- добавлена поддержка мульти-миров при запуске сервера и в нужном месте (а то юзеры по типу galaxy773 пишут свои загружалки мира, но не учитывают многие факторы, ну например, не распространяются настройки `world-settings` в некоторых кфг форко-ядер);
- добавлена поддержка системы лицензий OwlsLauncher;
- добавлено под-кэширование информации;
- документация нам не к чему;
- заренеймлено ядро и то что никто не ренеймит;
- импортирован фикс ttProxy и иных краш-систем/клиентов/ботоводеров;
- импортированы всеми нужные и популярные утилки по bukkit'у (ими обязательно пользуемся и поэтому все library плагины переписываем);
- исправлены критические ошибки в netty (из-за них можно было обойти проверки кучи плагинов, а потом чё угодно творить, вплоть до дюпов, никто не фиксит это почему-то);
- оптимизация проверок с известным результатом;
- отключена большая часть логирования информации;
- отключёны оставшиеся сливы статистики в веб;
- переведены некоторые сообщения логов;
- проверка на лицензию обесполезнена;
- свыше сотни команд кастрированы;
- скорректированы параметры по умолчанию в конфигурациях;
- удалены все проверки обновлений.

Маленько патчей для творения 😭, но что поделать, таковы цели ядрышка 👌 - не велики горы бытия. 🏔

# 💰 | По чём башлять?

Ядро имеет свою ценность и готово продаваться для коммерческого и народного пользованья, причём, без лицензии, но с обновлениями персональными подстать.  
💸 Объявленная ценность ядра: 50 000 ₽  

📞 Контакты для покупки: [developer](https://naulbimix.t.me).