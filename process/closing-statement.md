# XYZ

(Note: throughout this text, I’ll be linking to [process materials](https://github.com/pippinbarr/lets-play-ancient-greek-punishment-the-twine/blob/master/process/README.md) generated as part of the project in its [code repository](https://github.com/pippinbarr/lets-play-ancient-greek-punishment-the-twine). This approach to process documentation is part of the [Games as Research](https://www.gamesasresearch.com/) project.)

[_Let's Play: Ancient Greek Punishment: The Twine_](https://pippinbarr.github.io/lets-play-ancient-greek-punishment-the-twine) is the ninth edition in the "Ancient Greek Punishment" series I've been working on since 2011. Lately I've been interested in what happens when I retell the five mythological punishments using the "language" of different game engines, and this time around the game engine in question is Twine, an easy-to-use and highly accessible tool for creating hypertext stories.

Each of the myths has the character of being an infinite punishment scenario, the most famous probably being Sisyphus, doomed to push a boulder up a hill only to see it roll back down over and over again. Twine has its own character as a game/story creation tool, in terms of everything from its default stylesheet, to its underlying coding language of "macros", to the typical ways the Twine community uses Twine's features to create their stories. I'm always interested in the intersection between design and the technology in use, so in the following, I want to look particularly at each specific myth and how it interacts with the capacities of Twine through my own design decisions.

## Sisyphus's cyclical situation

I'm not 100% sure why, but I view the "[cycling link](https://twinery.org/wiki/harlowe:cycling-link)" as the emblematic storytelling technique in Twine stories. It's often used in stories in a couple of ways, but perhaps most interestingly as a way to create agency for the reader in determining the actual description of a scene. By cycling through the possibilities of the link, they can set a particular descriptive passage the way they like it, perhaps making a vase contain peonies instead of roses, say.

In planning to make these punishment games in Twine, it was immediately obvious to me that the _cycling_ part of the cycling link would be a great affordance to leverage - after you've seen all the possibilities of the link, it goes back to the first and continues on. As such, it's ideal for representing an endlessly repeating set of options, or in this case _actions_. So Sisyphus's pushing of the boulder is encoded as a cycling link - each advance of the link gets the boulder further up the hill, until the final option sends it rolling back to the bottom, leaving the player back where they started. The code looks like this:

![](images/sisyphus-code.png)
The Twine code for the cycling link in Sisyphus

Something that interests me here and elsewhere in the game is the physicality that you can interpret as part of the interaction here. Each click on the link (or touch on a mobile device) represents a literal _push_ of the boulder in the story - the player exerts effort, however minimal, to advance the text and the boulder itself, the text _is_ the boulder, the cycling link _is_ Sisyphean.

## The apple of your eyes only



## The role of the Promethean reader

Eco and role of the reader, open and closed texts

## Patterns of hypertext bathwater

[Patterns of Hypertext](https://www.eastgate.com/patterns/Patterns.html) [Cycle](https://www.eastgate.com/patterns/Patterns3.html)


## Additive infinity and immobility


---

Possible themes
- Agency
- Affordances (studying the list of macros)
- Physicality
- Mappings
- Writing style and pithiness
- A "typical twine"
- Cycles and infinite accumulations

- Tantalus
  - Mouse/finger movement as reaching, clicking as grasping*
  - Subtractive agency???
  - Failed actions in Twine
  - "Truth" of action? Action in the action or action in the text?
  -

- Prometheus
  - Inaction, no agency*
  - No struggle
  - Inevitability
  - Being done to
  - Time cycle
  -

- Danaids
  - Classic hypertext cycle (structure from Bernstein)*
  - Clicks as individual acts, typical form
  - Very dissociated from the actual physical acts of the story
  -

- Zeno
  - Additive infinity*
  - Flawed in terms of an inevitable overflow? Is there one? Is there a string limit? A webpage limit? The fact I don't know is the problem?
  - Most complex code underlying it
  - Still premised on a specific macro, but significantly more fiddly
  - (Maybe it's worth showing the code for each?)
  - Novel solution to Zeno (additive rather than cyclical) - because I couldn't use the cycle structure again in good faith
  -
