# Saint George and the Dragon of Silene

A small, kid-friendly adventure game in a single HTML file (`index.html`). Open it in any modern browser. Keyboard, gamepad and touch screens all work.

## Controls

**Move:** Arrows / WASD / left stick / D-pad · **Talk & Sword:** Space / E / Enter / Z (gamepad A, touch A) · **Holy Spear:** F (gamepad B, touch SPEAR, shown once the spear is joined) · **Dash:** C / Ctrl (gamepad Y, touch DASH) · **Block:** hold Shift / X (gamepad X, LB / RB, touch shield) · **Pause, Quest Log & Side Quests:** P / Esc / Q / Tab (gamepad START, touch ☰) · **Restart:** from the pause menu (R while paused, press twice to confirm) · **Music on/off:** N (touch ♪) · **Voices on/off:** V · **Mute everything:** M · **Horse on/off:** H (gamepad L3 = press the left stick, or a quick tap of D-pad Up; touch 🐴) · **Auto-continue text on/off:** T (or **Auto-continue** in the pause menu, which also works on touch screens and gamepads) · **Use a tool (v16):** G (gamepad RT, touch tool button next to A) · **Pick a tool:** 1 Axe, 2 Pickaxe, 3 Fishing Rod, 4 Bow (gamepad LT = next tool, touch: tap the tool slot at the top)

- The **sword** works on wolves, bears, snakes, bats, spiders, scorpions and rats, but it can't hurt the dragon ("Clink!").
- When George finds both pieces, the Holy Spear is **made whole again by a miracle from God**: a soft beam of light from heaven, gentle chimes and "A miracle! By God's grace, the Holy Spear is made whole again!"
- The **Holy Spear** has longer reach, a holy glow and a slightly slower cooldown. It is the only weapon that can hurt the dragon.
- The **dash** moves George about 3 tiles very quickly. He can't be hurt during a dash, but he still can't go through walls or trees. You can't dash while blocking or carrying a hen.
- **Tools (v16)** are bought from Smith Sam's Tool Shop. The tool button is *context-sensitive*: next to a little ribboned tree it uses the axe, next to a cracked rock the pickaxe, facing water the fishing rod, and anywhere else the tool you picked (usually the bow). The HUD shows the tool in a slot at the top.
- The **pause screen** freezes the game and shows the Quest Log, the Side Quests and the controls. It has Resume, Music, Voices, **Auto-continue**, **Test voice 🔊** and Restart. Use D-pad/stick + A to choose; START, B or Esc goes back to the game.

## Music and voices

- The music is original and made live with Web Audio. There are themes for the village, castle, cave, dragon lair and victory, plus the **Silene Hymn**, a gentle 3/4 organ-and-guitar hymn that plays during the prayers. The music is quiet during the storm, softly crossfades between places and gets quieter during speech and pause.
- The characters speak their lines with the browser's built-in speech voices (speechSynthesis), and each character has its own voice, pitch and speed. The prayers (the Hail Mary prayed by Princess Sabra and the Our Father in the little church, each starting and ending with the Sign of the Cross) are read slowly, and each page turns only after it has been fully read. If the browser has no voices, the text still shows and the pages turn when A is pressed or after a few seconds.
- **Reading pace:** the voices read about **15% slower** than before, which makes it easier for young readers to follow along. Each character still has their own pitch, and no voice goes below speed 0.75 (iPhone/iPad Safari uses the same values). Prayers and Grace are read at a calm 0.78. While a voice is speaking, the dialogue text types out at about reading pace instead of racing ahead. A / Space / tap still shows the whole line at once and then moves on.
- Sound, music and voices start after the first key, tap or click. On phones and tablets the **Tap to start** tap also unlocks speech and Web Audio (mobile browsers only allow sound that starts inside a real tap). The touch buttons speak right away inside the tap, and the game gently nudges the speech engine so long lines don't stall. If you can't hear any voices, open the pause menu and choose **Test voice 🔊**. George should say "Hello! I am George…".
- **iPhone / iPad: no sound?** The **Ring/Silent switch** on the side of the iPhone mutes Web Speech *and* web audio in Safari. Flip it to Ring (no orange showing) and turn the volume up, then tap Test voice. They can be turned off with N, V or M, or from the pause menu.

## Auto-continue text (autotext v13)

- Off by default. Turn it on with **T** or **Auto-continue: ON/OFF** in the pause menu. The game remembers the setting in this browser (localStorage).
- When it is on, each dialogue page turns by itself once the text has finished typing **and** the voice has finished reading it (with a short half-second pause after). With voices off or unavailable, the page waits a reading time of **1.2 s + 0.055 s per letter**, tuned for children who are learning to read. The last page closes the conversation by itself.
- It also works for the prayers, the Grace at Old Martha's and the feast.
- **Choices and menus never auto-pick.** The baker's shop and any question always wait for the player. (The donation boxes have no menu any more: one press gives one coin, and nothing is given unless you press.) The Tool Shop menu also waits for you.
- A / Space / tap still turns the page straight away.
- While it is on, a small green **▶▶** badge shows on the dialogue and prayer boxes.
- On iPhone/iPad, where the "voice finished" signal sometimes never arrives, the page still turns after the time the line should have taken to read aloud.

## What's new in v16

- **Smith Sam's Tool Shop (toolshop v16).** A new stall with a blue awning and a **TOOLS** sign, next to Old Martha's food stall in the village square. Talk to Smith Sam and a menu opens (it never picks for you; choose with ↑↓ + Space, the D-pad + A, or a tap). Each tool is bought **once** and then shows **Owned ✔**.

  | Tool | Price | What it does |
  |---|---|---|
  | Axe | 6 coins | chops the little trees with a red ribbon |
  | Pickaxe | 10 coins | breaks the cracked grey rocks |
  | Fishing Rod | 14 coins | catch fish in the river or the lake |
  | Bow & Arrows | 20 coins | shoots arrows the way George is facing |

  Not enough coins: *"You need N more coins."* Already bought: *"You already have it!"*
- **Secret places.** Six small hidden spots, each with a treasure chest (4–8 coins), are closed off by a ribboned tree (**axe**: the Woodcutter's Glade in the north, a Hidden Garden with a pear tree in the South Wood, the Lakeside Grove) or a cracked rock (**pickaxe**: a Mountain Garden with carrots, the Old Miner's Nook, the Secret Crystal Cave in the south-east mountains). A small hint ("G: chop" / "G: break") shows when you stand next to one. "Timber! A new path!" / "Crack! The rock breaks!" Once opened they **stay open** for the rest of the game, even after fainting or a night's sleep. None of them is ever needed to finish the game: every quest, chest and boss can still be reached without any tools (checked by the tests).
- **Fishing.** Face water and press the tool button: George casts, the bobber floats and bobs, then a **!** pops up. Press again quickly to reel in. Too early: "Too soon! Wait for the !". Too late: "It got away! Try again.". Walking away puts the rod away. A catch is usually a fish (+1 heart) or a big fish (+2 hearts), sometimes a little bag of coins (1–3 coins, never more than 12 in a whole game) or an old boot ("An old boot! Pee-yew!"). When George's hearts are already full, he lets the fish swim home.
- **Bow & Arrows.** Shoots an arrow straight in the facing direction (also on the horse). An arrow does **1 damage, the same as one sword hit**, with a slower reload (0.55 s) and unlimited arrows. **The dragon can't be hurt by arrows** ("Clink! Arrows bounce off dragon scales!"), so the Holy Spear is still the only way to win. Arrows stop at walls and trees.
- **One shared donation total (onegift v16).** The church alms box and the box at Saint Peter's Shrine now add to **one** total, and both signs show the same "Given: N". Giving coins **no longer fills hearts**. Milestones (combined): **10** = God blesses George's sword and shield, **25** = the church gets its golden bell, window and candles, **50** = Saint Peter's Shrine becomes **Saint Peter's Chapel**, **100** = a **Feast for Jesus** in the village.
- **Saint Peter's Shrine and Saint Peter's Chapel.** The little wayside shrine by the river is now **Saint Peter's Shrine**: a statue of Saint Peter (brown robe, white beard, a golden key) with a plaque, a signpost reading "Saint Peter's Shrine", and "Saint Peter's Shrine Box" for the offering box. Thanks there: "Saint Peter, pray for us!" At 50 coins: *"Saint Peter's Chapel is built! Thanks be to God!"*. The new chapel has a "SAINT PETER'S CHAPEL" sign by the door, and the signpost and box sign change to "Saint Peter's Chapel".
- **A Feast for Jesus (feast v16).** When the shared total reaches **100 coins**, the whole village gathers in the square: long tables with food, banners and bunting. Father Ambrose leads everyone in **Grace**, starting and ending with the **Sign of the Cross**, and says *"Thanks be to God! Today we feast in honor of Jesus!"*. Then everyone eats and chats, and you go straight back to play. The banners and tables stay up in the square afterwards. It works with voices on or off and auto-continue on or off (A always turns the page).
- **Day and night (night v16).** After every **30 minutes of active play** (the clock only runs while you are walking around: not when paused, talking, in a menu, a cutscene or a boss fight) the sun sets: *"The sun goes down. Time to rest!"*. Stars and the moon come out, George lies down to sleep (and Mia too, if she is with him) with floating **Zzz**, says a short prayer (*"Good night, God. Thank You for today. Amen."*), the screen fades, and the sun rises: *"Good morning! George feels strong again."*.
  - On waking: **all hearts are full, all fruit has grown back, and the wild creatures come back** (wolves, bears, snakes, crocs, bats and the other critters, and the white mini-bosses too). Quest bosses that have been beaten stay gone, exactly like after fainting, so no progress is ever undone: King Hissalot doesn't come back once the Snake King quest is won, the guardians of a Green Dragon chest don't come back once its piece is taken, and the dragon never comes back. Spear pieces, chests and gear that were already found stay found. Creatures are moved at least 200 px away from George so he never wakes up next to one.
  - Night only starts at a safe moment: outside in the open world (not in the castle, cave or a house), with no boss near and no creature close by, and not during a talk, menu, prayer or fishing. Otherwise it waits.
  - A small **sun clock** at the top of the screen shows the minutes until sunset. A (or a tap) skips ahead during the night scene.
  - For testing, `?daylen=60` in the address (or `sgNight()` in the browser console) makes night come sooner.

## What's new in v15

- **Give a coin with every A press (donate v15).** Stand at the **church alms box** or the new **offering box at Saint Peter's Shrine** (just right of the shrine path) and press **A** (Space / E / Enter / Z, the controller A button, or the touch **A** button). Each press gives exactly **one coin**, with a coin clink and a little **+1 ✝** and "Thank you!". There is no menu, so you can tap as fast as you like. A small sign over the box shows **"Given: N"**. It works **at any time**, from the very start of the game until the dragon is beaten. (After the dragon the Victory screen goes back to the title, so there is no more play to give in.) Pressing A at a box never swings the sword.
  - With no coins: *"You have no coins. God loves a cheerful giver!"* (said gently, only once in a while).
  - Voices don't pile up: thanks are spoken at most every few seconds while you tap. Milestones are always spoken.
  - **Church rewards:** at **10 coins** God blesses George's **sword and shield** (blessgear v15). It happens once, with soft chimes, a beam of light from above, and *"God has blessed your sword and shield!"* From then on both have a soft golden-white glow: in the world, while swinging and blocking, on and off the horse, and in the HUD. The glow is just for looks; it adds no extra strength. It does not repeat every 10 coins. At **25** the church gets its golden bell, new candles and stained-glass window.
  - **Shrine rewards (changed in v16):** the shrine box and the church box now share one total, and giving never fills hearts. At **50** coins Saint Peter's Shrine becomes **Saint Peter's Chapel** (see below). The Victory screen shows the total given.
- **Saint Peter's Chapel.** At 50 coins Saint Peter's Shrine is replaced by a much bigger stone chapel. It has a red roof, a bell tower with a swinging bell and a golden cross, an arched door facing the path, two stained-glass windows, a "Saint Peter's Chapel" sign by the door, and candles and flowers. Its walls are solid. It sits on open grass around the old shrine (no trees, fruit plants, chests or critters there). The path still leads to its door, there are ways around both sides, and the offering box stays outside by the path. Anyone standing where the chapel appears (George, Mia, critters) is moved safely onto the path in front of it.
- **Mia rides with you (miahorse v15).** While Little Mia is following George and he gets on the horse, Mia hops up and sits behind him on the horse, facing the same way, instead of running after it. When George gets off (H, the horse button, L3/D-pad up, or going indoors), she hops down next to him, never inside a wall or tree, and follows on foot again.

## What's new in v14

- **No more stuck zoom on iPhone (nozoom v14).** Fast taps on the touch buttons used to zoom Safari in, and it stayed zoomed. The page is now locked at 100%: no double-tap zoom, no pinch zoom, no scrolling, no text-selection pop-ups. If Safari ever does end up zoomed, the game snaps back to normal by itself. Holding the joystick while pressing A (two fingers) still works.
- **A slower storm.** Every storm caption stays on screen for at least 4 seconds (2 s + ½ s per word) and never moves on before the narrator has finished reading it. Then press **A / Space / tap** for the next caption, or let it move on by itself with Auto-continue ON. The rain, wind and thunder keep going while you read.
- **The Holy Spear is made whole by a miracle.** When George has both pieces, light shines down from heaven, soft bells chime and the narrator says "A miracle! By God's grace, the Holy Spear is made whole again!"
- **God's blessing, not magic.** Grandma's egg and Shepherd Ben's woolly scarf are now gifts "blessed by God", and the Green Dragon gear is blessed by God too.
- **Sign of the Cross.** The Our Father (with Father Ambrose) and the Hail Mary (with Princess Sabra) now start and end with "In the name of the Father, and of the Son, and of the Holy Spirit. Amen.", just like Grace Before Meals.

## The horse

- George has a **white horse with a red-and-white saddle cloth** from the very start. Press **H** (gamepad **L3** or a quick tap of **D-pad Up**, touch **🐴**, which sits just above-left of the A button in the right-hand action cluster) to hop on or off.
- Riding is **1.8× faster**, with a gallop animation and hoofbeats. The sword, block and Holy Spear all work while mounted, but you **can't dash** on the horse. The horse bumps into walls, trees and water just like George.
- Indoors (the castle, the bat cave and the dragon lair) **George ties up his horse** automatically. He also hops off to pray. You can't toggle the horse during a conversation or while carrying a hen.
- D-pad Up only toggles the horse on a **quick tap** (under about ¼ second). Holding it still walks George upward.

## Critters (all friendly-cartoon, all run away)

All of them do **half a heart** of damage, and the shield blocks them. Every one that runs away counts in the end tally.

- **Wolves, bears and snakes** are the same as before.
- **Bats** (bat cave) now take **2 hits**. The first hit flashes them and knocks them back ("One more hit!").
- **Spiders** (bat cave, 6 of them) take **1 hit**. Some dangle from the ceiling on a silk thread and drop down when George walks underneath. Others scuttle in quick zig-zags. There are cobwebs in the corners of the tunnel.
- **Scorpions** (the desert, 7 of them, plus a few more in the new Badlands) take **2 hits**. They wander about, raise their tail with a "!" as a warning, and then jab. They never walk onto the village roads.
- **Rats** (north, around the magpie grove where the golden cross lies, 7 of them) take **1 hit**. They nibble, dart about in little bursts, and rush George when he comes close. A hit sends them off with a squeak. They never block the cross.

- **Crocodiles** (3 at Silver Lake, 3 along the river, plus the big White Croc) rest half under water with only their eyes and snout showing. When George comes near the shore, a croc **opens its jaws wide first** (a flashing ring around them is the warning), then **snaps forward** onto the bank and slides back into the water. A snap does **half a heart** and the shield blocks it. They take **3 hits**, and when beaten they splash and swim away. Crocs never sit by a bridge, the fishing dock or the village. They count in the end tally too.

## The bigger world

The land is now almost **twice as big** (100 × 72 tiles). Everything from before is still in the same place, and the new lands join up with roads and signposts:

- **Silver Lake** (north-east): a big blue lake with a **fishing dock**, a rowboat and **Fisher Finn**. Crocodiles live here.
- **The Meadows** (south): wildflowers, the river running south and a turning **windmill** with **Miller Molly**.
- **The Ruined Tower** (south-east, up in the **mountain pass**): an old ivy-covered watchtower. **Hermit Hugh** lives on the pass.
- **Saint Peter's Shrine** (south, by the river): a little stone shrine with a statue of Saint Peter and candles. At 50 coins given it becomes Saint Peter's Chapel.
- **The Badlands** (east): sand, rocks and scorpions.
- **Southwood** (far south-west): a dark wood with a snake den.
- **Old Martha's food stall** stands just south of the village.

More wolves, bears, snakes and scorpions roam the new lands, and there are coin chests to find.

## The Green Dragon set

Four pieces of **Green Dragon** gear, blessed by God, are hidden in guarded chests in the new lands. A guarded chest only opens once its guardians have been driven off. The guardians stay near their chest and give up the chase if George runs far away.

| Piece | Where | Guardians |
|---|---|---|
| **Armor** | on Silver Lake's shore | the **White Croc** (5 hits) |
| **Helmet** | below the ruined watchtower | 3 **white wolves** (3 hits each) and a big **white bear** (6 hits) |
| **Gloves** | the Badlands scorpion nest | 4 scorpions and the big **White Scorpion** (4 hits) |
| **Boots** | the Southwood snake den | little snakes (1 hit) and the **White Cobra** (4 hits, a smaller lunge than King Hissalot's) |

- **Dragon fire** normally burns **1 heart**. Each piece takes away **¼ heart**: 1 piece = ¾, 2 = ½, 3 = ¼, and with **all four** pieces dragon fire **can't hurt George at all** ("The full Green Dragon set! Dragon fire can't hurt you now!"). The hearts at the top show the quarter and half hearts. The shield still blocks fire from the front.
- **Boots:** George walks about 10% faster on foot. **Gloves:** his sword swings a little faster.
- George's sprite shows every piece he has: green scale armor, a green helmet with a gold crest, green gloves and green boots. The pause screen shows **Dragon Set n/4** with a check box for each piece.
- Pieces and opened chests are kept if George faints. Guardians only come back for pieces that are still missing.

## Coins, Old Martha's stall and the alms box

- **Coins** come from chests (46 in the coin chests) and a few from critters that run away (a wolf gives 1, the big guardians 3, King Hissalot 5). The coin count is on the HUD and the pause screen. Coins never go below zero.
- **Old Martha's food stall** (just south of the village). Talk to Martha and choose with the D-pad/stick or arrows + A / Space, or tap a choice. B / Esc closes.

  | Food | Cost | Does |
  |---|---|---|
  | Fresh Bread | 2 | +1 heart |
  | Roast Chicken | 4 | +2 hearts |
  | Apple Pie | 6 | all hearts full |
  | Hearty Feast | 15 | +1 **max** heart (only twice) |

  Martha won't sell you food when your hearts are already full, so no coins are wasted. **Every bought meal starts with Grace**: George bows his head and the Grace is shown and read aloud slowly, *"In the name of the Father, and of the Son, and of the Holy Spirit. Amen. Bless us, O Lord, and these Thy gifts, which we are about to receive from Thy bounty, through Christ our Lord. Amen."* Then he eats and the hearts fill up. A / Space / a tap turns the pages quickly, but Grace is always shown.
- **The church alms box** (beside Father Ambrose's church) and **the Saint Peter's Shrine box**: press **A** once per coin (v15). Father Ambrose thanks you out loud. At **10 coins** at the church, God blesses George's sword and shield and they glow softly. At **25** the church gets a **golden bell, a stained-glass rose window and candles** by the door. Both boxes share one total (v16) and giving doesn't fill hearts. At **50** Saint Peter's Shrine becomes Saint Peter's Chapel, and at **100** the village holds a Feast for Jesus.

## Fruit instead of hearts

There are no floating heart pickups any more. **Fruit plants** grow all over the land instead: apple trees, pear trees, berry bushes, carrot patches and pumpkins. Walk up and press A (Space / tap) to pick. Fruit gives **+1 heart**, and a pumpkin gives **+2**. A picked plant grows back after about **60–90 seconds**. When your hearts are full, George says "You're already full!" and the fruit stays on the plant. Critters that run away sometimes drop an **apple**. (Grace is said for meals bought at Martha's stall, not for fruit picked along the way.)

The plants are spread out (at least 8 tiles apart) over every part of the map. There is always some fruit **just before every boss and guardian fight** (the dragon's tunnel, the White Wolf, the White Bear, King Hissalot and the four Green Dragon guardians), far enough away that the boss doesn't notice you while you eat.

## Little Mia

Mama Rose's daughter **Mia** has wandered **deep into the West Forest**, to a hidden flower clearing on its far west side. Mama Rose says so when you talk to her. Mia follows George home and Mama Rose thanks you. When George rides the horse, Mia sits behind him on it, and she hops off when he gets down (v15).

## The Victory Feast

After the dragon is tamed, everyone gathers in the castle hall for a **Victory Feast**. On the banquet table there are roast chicken, bread, fruit, pies and goblets. At the table sit the King, Princess Sabra, Father Ambrose and the villagers, including Mama Rose and Little Mia, and the horse waits at the doorway. Everyone bows their heads and Father Ambrose leads **Grace Before Meals**, shown line by line and read aloud:

> In the name of the Father, and of the Son, and of the Holy Spirit. Amen.
>
> Bless us, O Lord, and these Thy gifts, which we are about to receive from Thy bounty, through Christ our Lord. Amen.
>
> In the name of the Father, and of the Son, and of the Holy Spirit. Amen.

Then everyone eats. The food disappears and people chat over soft festive music. After that comes the victory screen. Every step continues with A / Space / a tap, and also moves on by itself, so the feast can never get stuck.

## Screenshots

v16: `screens/toolshop.png` (Smith Sam's Tool Shop menu), `screens/axe.png` (chopping open the Hidden Garden), `screens/pickaxe.png` (breaking into the Secret Crystal Cave), `screens/fishing.png` (a bite: the **!**), `screens/bow.png` (an arrow flying at a wolf), `screens/saint_peter_shrine.png`, `screens/shrine_upgrade.png` (Saint Peter's Chapel), `screens/feast_jesus.png` (the Feast for Jesus), `screens/night_sleep.png` and `screens/sunrise.png`.

v15: `screens/donate_church_v15.png` (A at the church box, 'Given: N'), `screens/donate_shrine_v15.png` (the shrine offering box), `screens/shrine_upgrade.png` (the 50-coin chapel, now Saint Peter's Chapel) and `screens/mia_horse.png` (Mia riding behind George) and `screens/blessed_gear.png` (the sword and shield blessing at 10 coins).


New v12 screenshots are in the `screens/` folder: `bigworld_overview.png` (the whole map with the fruit, chests, guardians and crocs marked), `bigworld_*.png` (lake, windmill, tower, shrine, pass, badlands, southwood), `armor.png`, `helmet.png`, `gloves.png`, `boots.png`, `fullset.png`, `fullset_world.png`, `shop.png`, `food_grace.png`, `food_eat.png`, `donate.png`, `donate_blessing.png`, `church_upgrade.png`, `fruit.png`, `fruit_pumpkin.png`, `crocs.png` and `crocs_white.png`.
