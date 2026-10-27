# Saint George and the Dragon of Silene

A small, kid-friendly adventure game in a single HTML file (`index.html`). Open it in any modern browser. Keyboard, gamepad and touch screens all work.

## Controls

**Move:** Arrows / WASD / left stick / D-pad · **Talk & Sword:** Space / E / Enter / Z (gamepad A, touch A) · **Holy Spear:** F (gamepad B, touch SPEAR, shown once the spear is joined) · **Dash:** C / Ctrl (gamepad Y, touch DASH) · **Block:** hold Shift / X (gamepad X, LB / RB, touch shield) · **Pause, Quest Log & Side Quests:** P / Esc / Q / Tab (gamepad START, touch ☰) · **Restart:** from the pause menu (R while paused, press twice to confirm) · **Music on/off:** N (touch ♪) · **Voices on/off:** V · **Mute everything:** M · **Horse on/off:** H (gamepad L3 = press the left stick, or a quick tap of D-pad Up; touch 🐴)

- The **sword** works on wolves, bears, snakes, bats, spiders, scorpions and rats, but it can't hurt the dragon ("Clink!").
- The **Holy Spear** has longer reach, a holy glow and a slightly slower cooldown. It is the only weapon that can hurt the dragon.
- The **dash** moves George about 3 tiles very quickly. He can't be hurt during a dash, but he still can't go through walls or trees. You can't dash while blocking or carrying a hen.
- The **pause screen** freezes the game and shows the Quest Log, the Side Quests and the controls. It has Resume, Music, Voices, **Test voice 🔊** and Restart. Use D-pad/stick + A to choose; START, B or Esc goes back to the game.

## Music and voices

- The music is original and made live with Web Audio. There are themes for the village, castle, cave, dragon lair and victory, plus the **Silene Hymn**, a gentle 3/4 organ-and-guitar hymn that plays during the prayers. The music is quiet during the storm, softly crossfades between places and gets quieter during speech and pause.
- The characters speak their lines with the browser's built-in speech voices (speechSynthesis), and each character has its own voice, pitch and speed. The prayers (the Hail Mary prayed by Princess Sabra and the Our Father in the little church) are read slowly, and each page turns only after it has been fully read. If the browser has no voices, the text still shows and the pages turn when A is pressed or after a few seconds.
- Sound, music and voices start after the first key, tap or click. On phones and tablets the **Tap to start** tap also unlocks speech and Web Audio (mobile browsers only allow sound that starts inside a real tap). The touch buttons speak right away inside the tap, and the game gently nudges the speech engine so long lines don't stall. If you can't hear any voices, open the pause menu and choose **Test voice 🔊**. George should say "Hello! I am George…".
- **iPhone / iPad: no sound?** The **Ring/Silent switch** on the side of the iPhone mutes Web Speech *and* web audio in Safari. Flip it to Ring (no orange showing) and turn the volume up, then tap Test voice. They can be turned off with N, V or M, or from the pause menu.

## The horse

- George has a **white horse with a red-and-white saddle cloth** from the very start. Press **H** (gamepad **L3** or a quick tap of **D-pad Up**, touch **🐴**) to hop on or off.
- Riding is **1.8× faster**, with a gallop animation and hoofbeats. The sword, block and Holy Spear all work while mounted, but you **can't dash** on the horse. The horse bumps into walls, trees and water just like George.
- Indoors (the castle, the bat cave and the dragon lair) **George ties up his horse** automatically. He also hops off to pray. You can't toggle the horse during a conversation or while carrying a hen.
- D-pad Up only toggles the horse on a **quick tap** (under about ¼ second). Holding it still walks George upward.

## Critters (all friendly-cartoon, all run away)

All of them do **half a heart** of damage, and the shield blocks them. Every one that runs away counts in the end tally.

- **Wolves, bears and snakes** are the same as before.
- **Bats** (bat cave) now take **2 hits**. The first hit flashes them and knocks them back ("One more hit!").
- **Spiders** (bat cave, 6 of them) take **1 hit**. Some dangle from the ceiling on a silk thread and drop down when George walks underneath. Others scuttle in quick zig-zags. There are cobwebs in the corners of the tunnel.
- **Scorpions** (the desert, 7 of them) take **2 hits**. They wander about, raise their tail with a "!" as a warning, and then jab. They never walk onto the village roads.
- **Rats** (north, around the magpie grove where the golden cross lies, 7 of them) take **1 hit**. They nibble, dart about in little bursts, and rush George when he comes close. A hit sends them off with a squeak. They never block the cross.

## Little Mia

Mama Rose's daughter **Mia** has wandered **deep into the West Forest**, to a hidden flower clearing on its far west side. Mama Rose says so when you talk to her. Mia follows George home (she keeps up with the horse too) and Mama Rose thanks you.

## The Victory Feast

After the dragon is tamed, everyone gathers in the castle hall for a **Victory Feast**. On the banquet table there are roast chicken, bread, fruit, pies and goblets. At the table sit the King, Princess Sabra, Father Ambrose and the villagers, including Mama Rose and Little Mia, and the horse waits at the doorway. Everyone bows their heads and Father Ambrose leads **Grace Before Meals**, shown line by line and read aloud:

> In the name of the Father, and of the Son, and of the Holy Spirit. Amen.
>
> Bless us, O Lord, and these Thy gifts, which we are about to receive from Thy bounty, through Christ our Lord. Amen.
>
> In the name of the Father, and of the Son, and of the Holy Spirit. Amen.

Then everyone eats. The food disappears and people chat over soft festive music. After that comes the victory screen. Every step continues with A / Space / a tap, and also moves on by itself, so the feast can never get stuck.
