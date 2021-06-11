# GMTK Game Jam 2021

> JOINED TOGETHER

About this jam:

- [GTMK 2021 on itch.io](https://itch.io/jam/gmtk-2021)
- [Theme announcement video](https://www.youtube.com/watch?v=XpzBfx45wUE)

# Instructions

This is a [TIC80 game](http://tic80.com/).

# Development

## Data Structures

Box:

- `c`: box color
- `x`: target x position
- `y`: target y position
- `px`: physical x position
- `py`: physical y position

Board:

- Matrix `HEIGHT * WIDTH` with possible values:
    - `w`: **w**all A.K.A. solid block
    - `b`: **b**ox
    - `nil`: nothing here, move as wanted

# DevLog

The theme was just announced, which means it's time to get working! So,
what could my game be about?

- One game where one controller works for many characters
    - This was done before a lot of times, like
      [Sisão](https://havana24.itch.io/sisao) and another one I forgot the name.
    - Characters may not necessarily be tied physically. Time or different
      controller schemes for the same character also work as well.
- Game about threads
    - They are all joined together, right? How could I make this happen though?
    - In this sense, I only think about mathematical knots, or the graphs made
      by carpet threads. Could these be related to puzzles though?
- A factory game about combining stuff
    - I think Biffa has already made a video on a
      [similar thing](https://shapez.io/), so I probably can't go on with that.
- Can this somehow be a card game? There probably is a way of making cards
  connected to each other and call this the theme...
- A puzzle game where all boxes must be tied together.
    - There could be a character pushing boxes around. Once two boxes are
      tied together, you have to move them together.
    - This could also be something that behaves like
      [2048](https://www.youtube.com/watch?v=9lIkyda3Fck):
      the boxes exist on this board and move together.
        - There could even be boxes that get separated and some that
          don't.
    - This feels too obvious to me though.
- What about an RPG where the effects are shared among everyone.
  For example: if you cause damage to one opponent, this damage is shared
  among everyone in the battle. The challenge then becomes how to kill your
  enemies without killing yourself.
    - Is this mathematically possible though? I feel like this is going to
      become a counting game in the end and this may not feel fun.

After one hour thinking about it, I think I will go with the following concept:

- The goal of the game is to get all boxes tied together
- Boxes always move to the same direction
- Yellow boxes get glued, blue boxes don't

Given that, I believe these are the main tasks:

- [x] Implement basic game
- [ ] Start creating puzzles
- [ ] Design game identity
- [ ] Implement quality of life features once puzzles are complete
- [ ] Make it pop!

When it comes to the basic implementation, I believe these should be the next
steps:

- [x] Draw sample board
- [x] Create data structure for sample level
- [ ] Implement movement for blue boxes
- [ ] Implement movement for yellow boxes
- [ ] Identify when level is complete
