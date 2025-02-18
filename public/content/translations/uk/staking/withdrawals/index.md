---
title: Виведення ставок
description: На сторінці наведено стислий опис виведення коштів під час стейкінгу, принципу роботи цієї функції, а також порядку дій стейкерів, які бажають отримати свої винагороди.
lang: uk
template: staking
image: /images/staking/leslie-withdrawal.png
alt: Носоріг Леслі з її винагородами за стейкінг
sidebarDepth: 2
summaryPoints:
  - Поліпшення Shanghai/Capella дало змогу виводити кошти під час стейкінгу на Ethereum.
  - Оператори валідаторів повинні надати адресу для виведення коштів, щоб увімкнути цю функцію.
  - Винагороди автоматично розподіляються кожні кілька днів.
  - Валідатори, які повністю виходять зі стейкінгу, отримають залишок балансу.
---

<UpgradeStatus dateKey="page-staking-withdrawals-when">
Функцію виведення коштів під час стейкінгу було запроваджено під час поліпшення Shanghai/Capella, яке відбулося 12 квітня 2023 року.&nbsp;<a href="#when" customEventOptions={{ eventCategory: "Anchor link", eventAction: "When's it shipping?", eventName: "click" }}>Докладніше про поліпшення Shanghai/Capella</a>
</UpgradeStatus>

Під **виведенням коштів під час стейкінгу** мається на увазі переведення ефірів (ETH) з облікового запису валідатора на рівні консенсусу Ethereum (Beacon Chain) на рівень виконання, на якому з ними можна здійснювати транзакції.

**Винагороди за залишок** понад 32 ETH автоматично й регулярно надсилатимуться на адресу виведення, яку пов’язано з кожним валідатором і надано користувачем. Користувачі також можуть **повністю вийти зі стейкінгу**, у такий спосіб розблокувавши свій загальний баланс валідатора.

## Винагорода за стейкінг {#staking-rewards}

Виплати винагород автоматично обробляються для активних рахунків валідаторів із максимально можливим ефективним балансом 32 ETH.

Будь-який залишок понад 32 ETH, отриманий через винагороди, фактично не внесе вкладу в капітал і не збільшить вагу цього валідатора в мережі, і тому автоматично виводиться як виплата винагороди кожні кілька днів. Ці винагороди не потребують жодної дії від оператора перевірки. Потрібно лише один раз надати адресу для виведення коштів. Усе це ініціюється на рівні консенсусу, а отже платити за газ (плату за транзакцію) на будь-якому кроці не потрібно.

### Як ми досягли цього? {#how-did-we-get-here}

Протягом останніх кількох років Ethereum пройшов кілька оновлень мережі, переходячи до мережі, захищеної самим ETH, а не енергозатратним майнінгом, як це відбувалося раніше. Участь у консенсусі на Ethereum зараз називається «стейкінгом», оскільки учасники добровільно заблокували свої ефіри (ETH), виконавши «ставку», щоб мати змогу брати участь у роботі мережі. Користувачі, які дотримуються правил, будуть винагороджені, тоді як спроби обману можуть призвести до покарання.

З моменту запуску контракту на депозити для стейкінгу в листопаді 2020 року кілька сміливих піонерів Ethereum добровільно заблокували кошти для активації «валідаторів» — спеціальних облікових записів, які мають право формально підтверджувати та пропонувати блоки відповідно до правил мережі.

До оновлення Shanghai/Capella не можна було використовувати поставлені ETH або отримувати до них доступ. Тепер ви можете за бажанням автоматично отримувати свої винагороди на вибраний рахунок, а також будь-коли вивести поставлені ETH.

### Як підготуватися? {#how-do-i-prepare}

<WithdrawalsTabComparison />

### Важливі зауваження {#important-notices}

Надання адреси для виведення коштів є обов’язковим кроком для будь-якого облікового запису валідатора, перш ніж він буде здатний вивести ETH зі свого балансу.

<InfoBanner emoji="⚠️" isWarning>
  <strong>Кожному обліковому запису валідатора можна призначити лише одну адресу виведення коштів, один раз.</strong> Щойно адресу вибрано й надіслано на рівень консенсусу, її не можна скасувати або змінити знову. Перевірте двічі приналежність і точність наданої адреси, перш ніж надсилати її.
</InfoBanner>

Ненадання цієї адреси <strong> не становить загрози для ваших коштів</strong>, якщо ваша мнемонічна/кодова фраза залишається в безпеці офлайн і не піддавалася жодним вторгненням або компрометації. Збій додавання облікових даних для виведення коштів просто призведе до того, що ETH залишаться заблокованими на рахунку валідатора доти, доки не буде надано адресу для виведення коштів.

## Повний вихід зі стейкінгу {#exiting-staking-entirely}

Зазначення адреси для виведення коштів є обов'язковим перед переказом _будь-якої суми_ коштів із балансу облікового запису валідатора.

Користувачі, які планують повністю вийти зі стейкінгу й вивести всі свої кошти, повинні також підписати та розіслати повідомлення про «добровільний вихід» з ключами валідатора, що запустить процес виходу зі стейкінгу. Це робиться за допомогою вашого клієнта валідатора, надсилається на ваш вузол консенсусу й не вимагає використання газу.

Час, необхідний для виходу валідатора зі стейкінгу, залежить від кількості інших валідаторів, які також виходять одночасно. Тому тривалість процесу виходу може різнитися. Після завершення процесу цей обліковий запис більше не несе відповідальності за виконання обов'язків мережі валідаторів, не має права на отримання винагороди й не має поставлених ефірів (ETH). Тепер обліковий запис буде позначений для повного виведення коштів.

Після позначення облікового запису для повного виведення коштів та надання відповідних даних для виведення користувачу потрібно лише чекати. Облікові записи постійно автоматично перевіряються пропонентами блоків на наявність коштів після вибуття зі стейкінгу, і ваш баланс буде повністю переказаний (ця операція також називається «повним виведенням») під час наступного <a href="#validator-sweeping" customEventOptions={{ eventCategory: "Anchor link", eventAction: "Exiting staking entirely (sweep)", eventName: "click" }}>проходження</a>.

## Коли активуються можливості виведення під час стейкінгу? {#when}

Можливості виведення під час стейкінгу доступні постійно! Функціонал виведення було активовано в межах оновлення Shanghai/Capella, яке відбулося 12 квітня 2023 року.

Оновлення Shanghai/Capella дало змогу повертати раніше вкладені ETH на звичайні облікові записи Ethereum. Це закрило коло стейкінгової ліквідності та привело Ethereum на крок ближче до створення стійкої, масштабованої, безпечної децентралізованої екосистеми.

- [Докладніше про історію Ethereum](/history/)
- [Більше про план розвитку Ethereum](/roadmap/)

## Як працюють платежі з виведення коштів? {#how-do-withdrawals-work}

Наявність чи відсутність у конкретного валідатора права на виведення визначається станом самого облікового запису валідатора. У будь-який момент визначення того, чи слід ініціювати виведення з облікового запису, відбувається без жодної участі користувача — процес виконується повністю автоматично на рівні консенсусу в неперервному циклі.

### Краще сприймаєте інформацію візуально? {#visual-learner}

Ознайомтеся з поясненням щодо функції виведення під час стейкінгу Ethereum від Finematics:

<YouTube id="RwwU3P9n3uo" />

### «Проходження» валідатора {#validator-sweeping}

Коли валідатору заплановано запропонувати наступний блок, він зобов'язаний створити чергу виведення, до 16 можливих виведень. Це робиться так: індекси валідаторів перебираються починаючи з 0, і для кожного визначається, чи є можливе виведення для облікового запису відповідно до правил протоколу. Якщо виведення можливе, обліковий запис додається до черги. Валідатор, налаштований на те, щоб пропонувати наступний блок, продовжить роботу з місця, де зупинився попередній, просуваючись впорядковано нескінченно.

<InfoBanner emoji="🕛">
Уявіть аналоговий годинник. Стрілка на годиннику вказує на годину та рухається в одному напрямку, не пропускаючи жодної години, і зрештою повертається до початку після досягнення останнього числа.<br/><br/>.
Тепер замість чисел від 1 до 12 уявіть, що на годиннику від 0 до N <em> (загальна кількість облікових записів валідаторів, які коли-небудь були зареєстровані на рівні консенсусу, понад 500 000 станом на січень 2023 року).</em><br/><br/>Стрілка на годиннику вказує на наступний валідатор, який потрібно перевірити на наявність коштів, що підлягають виведенню. Стрілка починає з 0 і просувається повним колом, не пропускаючи жодного облікового запису. Коли буде досягнуто останній валідатор, цикл розпочнеться з початку.
</InfoBanner>

#### Перевірка облікового запису на виведення коштів {#checking-an-account-for-withdrawals}

Коли ініціатор проходить валідатори й перевіряє їх на можливу необхідність виведення коштів, кожен валідатор, який перевіряється, оцінюється короткою серією питань, щоб визначити, чи слід викликати виведення коштів, і якщо так, то скільки ETH слід вивести.

1. **Чи була надана адреса для виведення коштів?** Якщо не вказано жодної адреси виведення коштів, рахунок пропускається, а виведення не ініціюється.
2. **Чи можна завершити роботу валідатора й вивести кошти?**Якщо валідатор повністю завершив роботу й ми досягли того, що особовий рахунок вважається «доступним для виведення», буде оброблено повне виведення коштів. Це переведе весь залишковий баланс на адресу виведення коштів.
3. **Чи максимально можливий ефективний баланс становить 32?** Якщо обліковий запис має облікові дані для виведення коштів, не повністю вийшов зі стейкінгу та містить винагороди більше за 32, буде оброблено часткове зняття коштів, яке передає лише винагороди понад 32 на адресу виведення користувача.

Існує лише дві дії, які виконуються операторами валідатора протягом його життєвого циклу, які безпосередньо впливають на цей потік:

- надання облікових даних для виведення, щоб дозволити будь-яку форму виведення;
- вихід із мережі, що призведе до повного виведення коштів.

### Без газу {#gas-free}

Цей підхід до виведення коштів під час стейкінгу не вимагає, щоб стейкери надсилали транзакції вручну для запиту на виведення певної суми ETH. Це означає, що **не потрібно сплачувати за газ (комісію за транзакцію)**, а виведення не конкурують за наявний блоковий простір виконавчого рівня.

### Як часто я отримуватиму винагороди за стейкінг? {#how-soon}

В одному блоці можна обробити щонайбільше 16 виведень. З такою швидкістю можна обробити 115 200 виведень валідаторів за день (за умови відсутності пропущених слотів). Як зазначено вище, валідатори без виправданих виведень буде пропущено, що скорочує час завершення процесу.

Розширюючи цей розрахунок, ми можемо оцінити час, необхідний для обробки певної кількості виведень:

<TableContainer>

| Кількість виведень коштів | Час до завершення |
| :-------------------: | :--------------: |
|     400,00        |   3,5 дня   |
|     500,00        |   4,3 дня   |
|     600,00        |   5,2 дня   |
|     700,00        |   6,1 дня   |
|     800,00        |   7,0 дня   |

</TableContainer>

Як бачите, цей процес сповільнюється зі зростанням кількості валідаторів у мережі. Збільшення кількості пропущених слотів може пропорційно уповільнити цей процес, але в загальному це буде представляти повільніший варіант можливих результатів.

## Часті питання {#faq}

<ExpandableCard
title="Коли адресу виведення вже вказано, чи можу я змінити її на іншу адресу?"
eventCategory="FAQ"
eventAction="Once I have provided a withdrawal address, can I change it to an alternative withdrawal address?"
eventName="read more">
Ні, процес надання облікових даних для виведення коштів є одноразовим, а адресу не можна змінити після надсилання.
</ExpandableCard>

<ExpandableCard
title="Чому адресу виведення можна встановити лише один раз?"
eventCategory="FAQ"
eventAction="Why can a withdrawal address only be set once?"
eventName="read more">
Коли адресу виведення встановлено на виконавчому рівні, облікові дані виведення для цього валідатора змінюються назавжди. Це означає, що старі облікові дані більше не працюватимуть, а нові будуть спрямовані до облікового запису на виконавчому рівні.

Адресами виведення коштів може бути смартконтракт (контролюється його кодом) або зовнішній обліковий запис (EOA, контролюється його приватним ключем). Зараз ці облікові записи не мають змоги передавати повідомлення назад на рівень консенсусу, що б сигналізувало про зміну облікових даних валідатора, а впровадження цієї функціональності додало б зайвої складності протоколу.

Замість зміни адреси виведення коштів для конкретного валідатора користувачі можуть установити як адресу виведення коштів смартконтракт, який може обробляти обертання ключів, як-от Safe. Користувачі, які налаштовують свої кошти до свого особистого зовнішнього облікового запису (EOA), можуть здійснити повне виведення для зняття всіх своїх зареєстрованих коштів, а потім знову зареєструватися, використовуючи нові облікові дані.
</ExpandableCard>

<ExpandableCard
title="Що, якщо я маю токени стейкінгу або беру участь в об’єднаному стейкінгу?"
eventCategory="FAQ"
eventAction="What if I participate in staking tokens or pooled staking"
eventName="read more">

Якщо ви є частиною <a href="/staking/pools/">пулу стейкінгу</a> чи маєте токени стейкінгу, вам слід звернутися до свого постачальника послуг, щоб отримати докладнішу інформацію про те, як здійснюється виведення стейкінгу, оскільки кожна служба працює по-своєму.

Загалом, користувачі повинні мати змогу повернути основні поставлені ETH або змінити постачальника стейкінгу, яким вони користуються. Якщо певний пул стає надто великим, кошти можуть бути виведені, викуплені та знову застосовані з <a href="https://rated.network/">меншим постачальником</a>. Або, якщо ви накопичили достатню кількість ETH, ви можете <a href="/staking/solo/">займатися стейкінгом вдома</a>.

</ExpandableCard>

<ExpandableCard
title="Чи відбуваються виплати винагород (часткові виведення) автоматично?"
eventCategory="FAQ"
eventAction="Do reward payments (partial withdrawals) happen automatically?"
eventName="read more">
Так, якщо ваш валідатор надав адресу для виведення коштів. Її потрібно надати один раз для початкової активації виведення коштів, після чого виплати винагород автоматично запускатимуться кожні кілька днів під час кожного проходження валідатора.
</ExpandableCard>

<ExpandableCard
title="Чи відбуваються повні виведення автоматично?"
eventCategory="FAQ"
eventAction="Do full withdrawals happen automatically?"
eventName="read more">

Ні, якщо ваш валідатор все ще активний у мережі, повне виведення не відбудеться автоматично. Для цього потрібно вручну ініціювати добровільне виведення.

Після завершення процесу виведення валідатора, якщо обліковий запис має дані для виведення, залишок коштів буде <em>виведений</em> під час наступного <a href="#validator-sweeping">проходження валідатора</a>.

</ExpandableCard>

<ExpandableCard title="Чи можу я вивести довільну суму?"
eventCategory="FAQ"
eventAction="Can I withdraw a custom amount?"
eventName="read more">
Виведення розроблені для автоматичного виконання, переносячи будь-яку суму ETH, яку не було внесено користувачем для стейкінгу. Це, зокрема, повний баланс для облікових записів, які завершили процес виходу.

Неможливо вручну запитати конкретну суму ETH для виведення.
</ExpandableCard>

<ExpandableCard
title="Я є оператором валідатора. Де я можу знайти додаткову інформацію щодо активації можливості виведення коштів?"
eventCategory="FAQ"
eventAction="I operate a validator. Where can I find more information on enabling withdrawals?"
eventName="read more">

Рекомендуємо операторам валідаторів відвідати сторінку <a href="https://launchpad.ethereum.org/withdrawals/">Виведення коштів зі стартової платформи</a>, де можна знайти докладну інформацію про те, як підготувати свій валідатор до виведення коштів, розклад подій, а також більше інформації про те, як функціонує виведення коштів.

Щоб спробувати налаштування спочатку на тестовій мережі, почніть роботу на <a href="https://goerli.launchpad.ethereum.org">стартовій платформі стейкінгу в тестовій мережі Goerli</a>.

</ExpandableCard>

<ExpandableCard
title="Чи можу я активувати свій валідатор знову після виходу, внісши додаткову кількість ETH?"
eventCategory="FAQ"
eventAction="Can I re-activate my validator after exiting by depositing more ETH?"
eventName="read more">
Ні. Після виходу валідатора й повного зняття його балансу будь-які додаткові кошти, внесені на цей валідатор, автоматично будуть переведені на адресу для виведення під час наступного проходження валідатора. Для повторного стейкінгу ETH потрібно активувати новий валідатор.
</ExpandableCard>

## Довідкові джерела {#further-reading}

- [Виведення на стартовій платформі стейкінгу](https://launchpad.ethereum.org/withdrawals)
- [EIP-4895: Протокол ланцюжка Beacon здійснює виведення як операції](https://eips.ethereum.org/EIPS/eip-4895)
- [Ethereum Cat Herders — Шанхай](https://www.ethereumcatherders.com/shanghai_upgrade/index.html)
- [PEEPanEIP #94: Виведення ETH під час стейкінгу (тестування) із Potuz і Hsiao-Wei Wang](https://www.youtube.com/watch?v=G8UstwmGtyE)
- [PEEPanEIP#68: EIP-4895: зняття коштів за допомогою маякового ланцюжка як операції з Алексом Стоуксом](https://www.youtube.com/watch?v=CcL9RJBljUs)
- [Розуміння ефективного балансу валідатора](https://www.attestant.io/posts/understanding-validator-effective-balance/)
