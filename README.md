# Saint George and the Dragon of Silene

A small, kid-friendly adventure game in a single HTML file (`index.html`). Open it in any modern browser. Keyboard, gamepad and touch screens all work.

## Controls

**Move:** Arrows / WASD / left stick / D-pad · **Talk & Sword:** Space / E / Enter / Z (gamepad A, touch A) · **Holy Spear:** F (gamepad B, touch SPEAR, shown once the spear is joined) · **Dash:** C / Ctrl (gamepad Y, touch DASH) · **Block:** hold Shift / X (gamepad X, LB / RB, touch shield) · **Pause, Quest Log & Side Quests:** P / Esc / Q / Tab (gamepad START, touch ☰) · **Restart:** from the pause menu (R while paused, press twice to confirm) · **Music on/off:** N (touch ♪) · **Voices on/off:** V · **Mute everything:** M

- The **sword** works on wolves, bears and snakes, but it can't hurt the dragon ("Clink!").
- The **Holy Spear** has longer reach, a holy glow and a slightly slower cooldown. It is the only weapon that can hurt the dragon.
- The **dash** moves George about 3 tiles very quickly. He can't be hurt during a dash, but he still can't go through walls or trees. You can't dash while blocking or carrying a hen.
- The **pause screen** freezes the game and shows the Quest Log, the Side Quests and the controls. It has Resume, Music, Voices and Restart. Use D-pad/stick + A to choose; START, B or Esc goes back to the game.

## Music and voices

- The music is original and made live with Web Audio. There are themes for the village, castle, cave, dragon lair and victory, plus the **Silene Hymn**, a gentle 3/4 organ-and-guitar hymn that plays during the prayers. The music is quiet during the storm, softly crossfades between places and gets quieter during speech and pause.
- The characters speak their lines with the browser's built-in speech voices (speechSynthesis), and each character has its own voice, pitch and speed. The prayers (the Hail Mary prayed by Princess Sabra and the Our Father in the little church) are read slowly, and each page turns only after it has been fully read. If the browser has no voices, the text still shows and the pages turn when A is pressed or after a few seconds.
- Sound, music and voices start after the first key, tap or click. They can be turned off with N, V or M, or from the pause menu.
