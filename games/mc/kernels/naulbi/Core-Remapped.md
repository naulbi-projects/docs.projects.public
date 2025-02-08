# Core-Remapped

# Что это такое?

`Core-Remapped` — это ядро:
- для <a href="https://minecraft.net/">Minecraft</a>, на игровую версию 1.12.2;
- собранное исключительно из исходных файлов всех форкнутых ядер <a href="https://hub.spigotmc.org/stash/projects/SPIGOT/repos/bukkit/browse">Bukkit</a> до <a href="https://github.com/PaperMC/Paper/tree/ver/1.12.2">Paper</a> с использованием необходимых библиотек и частично приведённых библиотек к исходникам;
- единственное в своём роде содержащее все "заремаппленные" исходники Vanilla (в том числе которые вечно не приводятся к исходникам в "бумаге" и летают в библиотеках) с исправлеными ошибками для компиляции;
- выполенное ручным "ремаппом" на основе <a href="https://github.com/PaperMC/Paper/tree/ver/1.12.2">Paper</a> с использованием: кастомных (лично созданных) "маппингов", "маппингов" от <a href="https://github.com/FabricMC/yarn/tree/1.12">FabricMC 1.12</a> и всевозможных "маппингов" из <a href="https://www.spigotmc.org/wiki/buildtools/">BuildTools</a> (как инструкции);
- переведённое из всех возможных кодовых баз форков по "OBFHELPER" в настоящий "ремапп";
- оптимизированное ядро: конструкциями языка программирования, сжатием кода и удалением неиспользуемого кода в ходе массового форкинга;

Этот проект предназначен для удобства взаимодействия с кодом игры и поддержкой возможных форков этого проекта для личного использования.

## Альтернативное, непонятное объяснение "Что это такое?" (от 26 июля 2022 г.)

`Core-Remapped` — Папер 1.12.2 с методами без обфускации и с улучшениями/исправлениями некоторых моментов, но основная цель заключается в корректном коде. В ядре ещё от разработчика нотча была оставлена обфускация названий методов, переменных и прочего, но это так и не исправили, лишь каждые кто делал патч добавляли OBFHELPER (метод с адекватным названием ссылающийся на обф метод, просто обф метод использовался в разных классах, а никто не хотел разбираться). Делаем это не патчами, а сурсами в интелию под граблями.

# Сроки разработки (UTC+3).

Официальная дата начала разработки: 25 июля 2022 г 23:23.  
Дата временного прекращения разработки: 12 января 2024 г. 22:53.  
Итого: **534 дня**.

![](/_img/games/mc/kernels/Core-Remapped/1.jpg)
![](/_img/games/mc/kernels/Core-Remapped/2.jpg)

# Канал "dev blog".

Для повествования обо всех изменениях в ядре был создан канал на платформе Telegram, в котором ежедневно публиковалась какая-либо информация, а также дата в формате "Ремапим Папер 1.12.2. День N.", где N - текущий день от начала создания данного творения.
На момент написания данной документации канал был удалён.

![](/_img/games/mc/kernels/Core-Remapped/devlog.jpg)

## Мнение о ядре.

В ядре произведено слишком много ненужных изменений (время потрачено бесполезно) и парочка псевдо-оптимизаций, которые в некоторых моментах могут замедлить ядро, поэтому требуется частичный откат, но ядро по-прежнему будет опережать в своей работоспособности стандартную "бумагу 1.12.2".  
В основных задачах входил "ремапп" и она на большую часть выполнена.

Статус ядра на момент написания документации: Недоделано, Архивный.

# Список изменений.
- [[27d4497]](https://github.loc:1337/VifePlay/Core-Remapped/commit/27d449766f046df6893072172f61b5c2c304c2c2) Загружены оригинальные исходники Paper; maven переделан в gradle; обновлены ссылки на репозитории maven
- [[76256a2]](https://github.loc:1337/VifePlay/Core-Remapped/commit/76256a2b3a78484b86cd10a7829bc6a31d9bc187) Загружен файл README.md
- [[86b6fb2]](https://github.loc:1337/VifePlay/Core-Remapped/commit/86b6fb28fac9568adb3a4fbf64cd52a0081e4214) Обновлены типы использования зависимостей; добавлены зависимости для tests; установлена кодовая система для компилятора gradle; добавлена версия Java для компилятора; <ins>по ошибке</ins> загружены кэш файлы + папка builds
- [[267dc7d]](https://github.loc:1337/VifePlay/Core-Remapped/commit/267dc7dbaeaf9eae0272d6a4993ebd510e76e183) Исходниками добавлена библиотеки **authlib**, **terminalconsole**; загружены исходники цветов от **md_5**; добавлен перевод папки `mojang-translations`
- [[62dd859]](https://github.loc:1337/VifePlay/Core-Remapped/commit/62dd859232979fe76a78ba664381017195d29aff) Попытка загрузки изменений по новой | Добавлен файл `.gitignore`; произведены изменения Array на Lists 🤡; добавлено принудительное использование **projectlombok**; добавлены исходники Vanilla (by Mojang); попытки оптимизации **terminalconsole**; удалена информация о MIT License; загружен файл `mojang-translations`.
- [[e417d1c]](https://github.loc:1337/VifePlay/Core-Remapped/commit/e417d1c844d24ce56ff09a6aa97bd2cecd8aa36b) `.gitignore` теперь игнорирует нужные файлы.
- [[6e84f53]](https://github.loc:1337/VifePlay/Core-Remapped/commit/6e84f53f0d4a233d2b7d7547d3ec1136bc6b869a) Протестирован gpg key.
- [[aec0259]](https://github.loc:1337/VifePlay/Core-Remapped/commit/aec0259d9b1f3a89fd4698d3afc461b7f1b9e380) Исправлена ошибка с зависимостями (lang3 и commons-codec) от **authlib**; использование for заменено на forEach в файлах **authlib** и переписано множество конструкций (Возможна деоптимизация⚠️)
- [[3f0d25e]](https://github.loc:1337/VifePlay/Core-Remapped/commit/3f0d25e19d8e74206b1324e33bb75af660f86f6c) Добавлены зависимости от minecraft-server (fastutil и jline-reader), а также удалено использование minecraft-server, как библиотеки; исправлены ошибки декомпиляции ✅; продолжение изменений for на forEach 🤡
- [[ed02296]](https://github.loc:1337/VifePlay/Core-Remapped/commit/ed02296da1e7df88da5efefff799fc7fcd5b5f7f) Добавлены комментарии к предыдущим исправления компиляции ✅; произведены попытки ремаппинга (advancement)
- [[4ffe6de]](https://github.loc:1337/VifePlay/Core-Remapped/commit/4ffe6deff125e3e69957d7df24dcbd4d91dbbdbc) Исправлена ошибка компиляции gradle проекта; удалены зависимости для tests; полностью исправлены ошибки декомпиляции ✅; произведены попытки ремаппинга; удалено tests
- [[783ebe2]](https://github.loc:1337/VifePlay/Core-Remapped/commit/783ebe2a560f03049f01260b28a1352bf135b00f) Изменён параметр group в gradle; добавлены дополнительные опции на исправления компиляции в gradle и для wrapper; изменён код gradlew; мелкие корректировки комментариев `Core-Remapped`; добавлена аннотация на класс утилок; скорректировано использование **projectlombok**
- [[de83de4]](https://github.loc:1337/VifePlay/Core-Remapped/commit/de83de4523b049c5df6cd28019c267ef99290a9b) Добавлен плагин **shadowJar**; исправлена ошибка типа компиляции некоторых зависимостей; за исключением **projectlombok** зависимости исходят из папки `libs`; добавлен файл `MANIFEST.MF`; попытки оптимизации кода через lambda; использование конструкций for на forEach 🤡; добавлены `assets`; удалены файлы `package-info.java`; перезалит файл от `mojang-translations`
- [[4694011]](https://github.loc:1337/VifePlay/Core-Remapped/commit/4694011ce156edec71f8427c1151abdc11686c53) Теперь аргументы для компилятора от **gradle** содержатся в списках; удалён контроль утилок; произведён рефакторинг с `net.minecraft.server` на `net.minecraft`  ✅
- [[d30c2fd]](https://github.loc:1337/VifePlay/Core-Remapped/commit/d30c2fda43088ad2411c02663bdec9dffb696790) Произведено изменение структуры пакеджей проекта: ачивки, блоки, команды, зачарования, энтити, скоребоард, звуки, утилки; произведён ремаппинг некоторых классов; исправлены ошибки доступа к коду в ходе изменения структуры проекта ✅
- [[dc89628]](https://github.loc:1337/VifePlay/Core-Remapped/commit/dc89628f8cd55bcdfd9d09ce4982c8687dae945b) Оптимизация проекта путём удаления не нужного кода полученного в ходе декомпиляции ⚠️
- [[7f8a2d0]](https://github.loc:1337/VifePlay/Core-Remapped/commit/7f8a2d0b33c4d8bad0e5abea27d060f5982d8b92) Начало ремаппинга ачивок ✅ Предупреждение о баге в ходе ремаппинга ❌
- [[323d7bc]](https://github.loc:1337/VifePlay/Core-Remapped/commit/323d7bcf1175086e222f641f5f54caf2d8d2187c) Исправлена предыдущего бага (полученный в ходе декомпиляции или ремаппинга???) ✅
- [[2149385]](https://github.loc:1337/VifePlay/Core-Remapped/commit/21493853fc6e9d961a8a4e4d2a9569e4f871d097) Ремаппинг ачивок и блоков. Фикс бага в ачивках. ✅
- [[ac00196]](https://github.loc:1337/VifePlay/Core-Remapped/commit/ac00196088f7fa3337d4d84ef2942a7e53d00452) Ремаппинг блоков и глобальные изменения одного класса блоков (названия схожие, поэтому много страшных изменений). ⚠️
- [[f9d4415]](https://github.loc:1337/VifePlay/Core-Remapped/commit/f9d4415be60be9e38211626ee5c269338cea20b7) Добавлено анти-игнорирование скомпилированного файла **".jar"**, но его в этом коммите не добавили; внеочередной ремаппинг блоков ✅
- [[017413c]](https://github.loc:1337/VifePlay/Core-Remapped/commit/017413ce2190324d2e244de2e4bf46e827b7a5f8) Ремаппинг блоков и наличие в билде бага ⚠️
- [[fd6561b]](https://github.loc:1337/VifePlay/Core-Remapped/commit/fd6561b113bc2c6635df810f2e2e2a4a8306640a) Фикс бага ✅; создание отдельного файла UserCache.java с не совсем хорошим рефакторингом; ремаппинг блоков
- [[722f852]](https://github.loc:1337/VifePlay/Core-Remapped/commit/722f8526755b88f53e6ea558355b4cc0e34db501) Небольшой ремаппинг блоков и глобальные изменения по ранее сломанному классу из коммита [[ac00196]](https://github.loc:1337/VifePlay/Core-Remapped/commit/ac00196088f7fa3337d4d84ef2942a7e53d00452).
- [[1517549]](https://github.loc:1337/VifePlay/Core-Remapped/commit/1517549dad02d5a7461b14ed71f1b88aa574965b) "Неизвестные мне изменения" по названию коммита; какие-то изменения по fields по блокам, но в итоге почему-то классы заново добавились, но не суть.
- [[29e533a]](https://github.loc:1337/VifePlay/Core-Remapped/commit/29e533a8171e4f7bcd194fdaac810f87edd09644) Глобальные реплейсы; ремаппинг 5 - 7 классов блоков
- [[bcfe528]](https://github.loc:1337/VifePlay/Core-Remapped/commit/bcfe5283462bcdb1e7e17df3a8427053240f87f0) Небольшой ремаппинг блоков из-за переустановки винды
- [[c2ca06e]](https://github.loc:1337/VifePlay/Core-Remapped/commit/c2ca06e55aae356a61f8e0ad6275e3f9fa8448cd) Загрузка каких-то старых изменений (я не работал 1 - 2 недели): мир, нетворкинг, nbt, статистика и что-то ещё; начало ремаппинга ???
- [[1cbf550]](https://github.loc:1337/VifePlay/Core-Remapped/commit/1cbf5506461f745eb3edb30da56d640d8e73e325) Небольшой ремаппинг блоков; корректировка try-catch конструкций использованием "ignored"; уменьшение кода по "return" | День 215
- [[39f766c]](https://github.loc:1337/VifePlay/Core-Remapped/commit/39f766cfec4eec1fc96276d157c0f064af2c4b4a) Рефакторинг блоков и актуальные исправления: небольшой рефакторинг `net.minecraft.block.`, удаление дюплицированного репо в **build.gradle** ✅, актуализация изменений по названию сервера и исправление прав доступа к методам/полям.
- [[7687962]](https://github.loc:1337/VifePlay/Core-Remapped/commit/7687962041751aa96b6b7ab7044781159d3c8683) Фикс Bukkit API ✅
- [[4b25e50]](https://github.loc:1337/VifePlay/Core-Remapped/commit/4b25e50d2c28a9cf6851da4aaa89284ef67227e4) Исправление CVE эксплойта в ресурс-файлах (уже новая версия либы, но всё равно) ✅
- [[23a2e1f]](https://github.loc:1337/VifePlay/Core-Remapped/commit/23a2e1fc2abdec58807425ebe4909ba42f7bb277) Небольшой ремаппинг "центральных классов" ядра (от `base-kernel`); актуализация версий зависимости аннотаций; небольшая математическая и чего-то в целом мелкого оптимизация
- [[1700fb1]](https://github.loc:1337/VifePlay/Core-Remapped/commit/1700fb1bad65100bfb24d312ee97040727ab4dc2) Небольшой ремаппинг "центральных классов"; обновление названия сервера; удаление неиспользуемого кода
- [[69b6755]](https://github.loc:1337/VifePlay/Core-Remapped/commit/1700fb1bad65100bfb24d312ee97040727ab4dc2) Реструктуризация кода из-за отступов
- [[7fb8e23]](https://github.loc:1337/VifePlay/Core-Remapped/commit/7fb8e2396b19db2b24662c2ff75ac6086d4b35ce) Актуализация версии gradle и его компиляторов; маленький рефакторинг в "центральном классе"
- [[2ee7f14]](https://github.loc:1337/VifePlay/Core-Remapped/commit/2ee7f1430e3c58888df8f03a49c89c2580b270e4) Исправление ошибки комментирования классов `Core-Remapper` -> `Core-Remapped` ✅
- [[ac9db2f]](https://github.loc:1337/VifePlay/Core-Remapped/commit/ac9db2f530e37340b16242c4303a83f088a2f88b) Фикс Bukkit API ✅
- [[3e8e1d2]](https://github.loc:1337/VifePlay/Core-Remapped/commit/3e8e1d25b60e0e86bdc804f585c997c70969977a) Обновление версии gradle
- [[9285135]](https://github.loc:1337/VifePlay/Core-Remapped/commit/9285135b6079f0c954d105e32a69c017587913ed) Фикс флага в gradle (не актуален стал) ✅
- [[3afa180]](https://github.loc:1337/VifePlay/Core-Remapped/commit/3afa1802220c944c16d3b7410029bcbf9e455178) Жалкая попытка оптимизации дюплицированного кода от CraftBukkit
- [[6814cf5]](https://github.loc:1337/VifePlay/Core-Remapped/commit/6814cf58e7b12e8ba88bc948df77367179f73fc9) Небольшие математические оптиимзации в блоках; глобальный ремаппинг логгеров в каждом из классов
- [[d750dc6]](https://github.loc:1337/VifePlay/Core-Remapped/commit/d750dc6580e3a06122e5c12ba390ba4fb0bbfa64) Обновление версии gradle на nightly (dev build)
- [[bedfea6]](https://github.loc:1337/VifePlay/Core-Remapped/commit/bedfea669abc1f5393b10bc27686248976c0a71e) Фикс, который доходил 2 года - фикс игнорирования билдовой папки ✅
- [[baaf598]](https://github.loc:1337/VifePlay/Core-Remapped/commit/baaf5983b6b01efa04b0bf38b3c88a54efac6032) Добавлены "**.jar**" файлы
- [[e8f4c00]](https://github.loc:1337/VifePlay/Core-Remapped/commit/e8f4c004d8d462020e9b7e40dced014772bff5be) Исправления коммента `Core-Remaopped` и небольшое удаление ненужного кода в классе утилок ✅
- [[fcbfc9d]](https://github.loc:1337/VifePlay/Core-Remapped/commit/fcbfc9d4a24175caf59a74052f21ffa4fa45f440) Рекомпиляция билд файла на Java 8; фикс компиляции из-за не отрефакторенного логгера ✅
- [[70dc8c9]](https://github.loc:1337/VifePlay/Core-Remapped/commit/70dc8c91c527bee4a033a59a866a1b1985c19ca9) Сбилженная жарка (shadowJar)
- [[af9103b]](https://github.loc:1337/VifePlay/Core-Remapped/commit/af9103bf63a195ed58fc193451a5735107abeeff) Актуализация версии gradle
- [[07bcb8a]](https://github.loc:1337/VifePlay/Core-Remapped/commit/07bcb8a9833d8363a18a8a7ce7933248d1c0fbc7) Исправлена NOTE от bukkit ✅
- [[a14dcb7]](https://github.loc:1337/VifePlay/Core-Remapped/commit/a14dcb7667c8b3a434f64b19b56fb27ef9a33006) Небольшая, общая оптимизация кода
- [[c855095]](https://github.loc:1337/VifePlay/Core-Remapped/commit/c855095ec0c3a62c9fae88c849518ece380e194f) Актуализация версии gradle
- [[721320b]](https://github.loc:1337/VifePlay/Core-Remapped/commit/721320bc9f256886388a8ae9e9273d9c0b3586e8) "Реальный рефакторинг"
- [[7e2e0de]](https://github.loc:1337/VifePlay/Core-Remapped/commit/7e2e0de6a267aa70fcbacb0e52a258090dd184c9) Фикс моего некорректного коммитинга ✅
- [[882868d]](https://github.loc:1337/VifePlay/Core-Remapped/commit/882868dbaaa343c7171693989ef1233dbdc7b780) Маленькая оптимизация блоков (fix ram leak) ✅
- [[18ee42f]](https://github.loc:1337/VifePlay/Core-Remapped/commit/18ee42fe6ed657cc11ee9aca6a55afcd75947941) Актуализация версии gradle
- [[b056d17]](https://github.loc:1337/VifePlay/Core-Remapped/commit/b056d17c18246c4da4c6b49cb25acf972d291545) Ремаппинг кода от PAILs (CraftBukkit) ✅
- [[d40786c]](https://github.loc:1337/VifePlay/Core-Remapped/commit/d40786c07986184ee6a662afa5c995c9edad3518) Оптимизация try-catch ("ignored") в утилках; оптимизация типов данных (int, char, double, float)