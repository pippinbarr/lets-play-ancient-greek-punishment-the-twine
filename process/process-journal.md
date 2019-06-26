# Opening salvo, style versus substance, twine affordances, designs?, and so (Tuesday, 25 June 2019, 15:47PM)

## Opening salvo

Hi. So because I've been working on an Inform 7 version of the punishment series, it seemed like a sensible idea to also give some thought to the Twine version, being in a text-y mindset etc.

It's also because part of me feels like I can maybe knock out a quick Twine version and thus delay releasing the Inform version which I'm still caught up in indecision over in terms of whether to "save" it for IFCOMP, submit it to sub-q, or just to put it Out There. Probably it'll be something like "submit to sub-q and get rejected" followed by "submit to IFCOMP and fail miserably" followed by "Put It Out There". So, everything.

Anyway that's neither here nor there, let's talk Twine.

It's probably silly to think I can do this quickly, nothing is quick.

## Big question: "style versus substance"?

One thing I've been thinking about when it comes to Twine is whether I should be focusing on making a Twine that is "like a Twine" and so looks like and feels like whatever a "standard" Twine looks and feels like that. So narrative-oriented, links as actions and expanding descriptors, and stuff like that. Perhaps in some sense "using Twine the way it's intended" or something.

On the other hand I could think more about using Twine as a platform/material/technology and so look at how the affordances of Twine as a language relate to the punishments, asking which elements of Twine are cyclical, reptitive, etc. This seems more obviously interesting to me, but could potentially yield something that "doesn't look like a Twine" which would slightly defeat the purpose. This is especially the case when I start thinking about this as a vehicle to make a kind of very typographic/concrete version of the game and complete that with fancy stylesheets so it just doesn't look very Twine-y.

I haven't quite settled that, but I think it's clear that I at least need to think about how the underlying affordances of Twine relate to the punishments. I can just have an "and then" kind of story, and obviously the punishments aren't really about CYOA decision-making (or they could be in a comedy way, but I don't think it's the right way in this context? Maybe it would be funny to have a downloadable CYOA version?).

So I suppose its "both" then. It should still be like a Twine I think (and so less obviously like something like Burnt Matches), but should ultimately rely on the underlying mechanics of Twine (and hypertexts in general) to represent cyclical/eternal punishments.

(This feels related to questions I've been thinking about relative to Inform 7's underlying world representation and having punishments be true to that world representation - the edible apple being the quintessential example of this kind of authenticity.)

## Twine affordances

The other day in a café I sat down to try to write down the various scripting hooks and other techniques that Twine (2) has available to put to work here. (Though now I say that I kind of wonder if Twine 1.whatever is a better tool given the number of extensions? Although is using all those extensions somehow less Twine-y?)

- Hyperlinks (the basic idea of passages/pages linked to one another)
- Cycling links
- Click to reveal links (and mouseoever variants) - Changers, links
- link-repeat maybe interesting in that it's iterative
- Variables saved and remembered
- Conditionals and loops (infinite loops?)
- Arrays
- Datamaps
- Datasets
- Dropdown menu and other UI elements (seems very UI though,)
- Undo (maybe something interesting about getting the player to click an undo link)
- Note that you can generate errors that might be of interest? Stack overflows? Non-existent destination passages?
- Live macros that are updated in real time
- event macro looks like it can handle timers?
- Mathematics
- alert and confirm and prompt
- Loading and saving games (this is another way to return to an initial state)
- Text manipulations, including rotation which could be funny in Sisyphus (but too concrete?)
- Transitions

So it's a pretty detailed set of possibilities? A lot of these aren't what I would call "typical" Twine techniques at the Twine-culture level necessarily, but still worth playing with? They are, after all, part of the language?

So look at the list I think these things:

- Part of Twine is creating a directed graph (of links), and that graph can be cyclical, and that can represent an experience that returns to its starting point. This idea of linking is, really, the fundamental nature of Twine, so it's appropriate to leverage it.
- A cycling link is another example of something that can return to its starting point (though in this case on a single page). After standard hyperlinking I think of it as the most emblematic Twine technique.
- Saving and restoring is kind of interesting. Under the hood you would be able to save the game in its incomplete/initial state, let them play through to a potential end point, and at the critical moment reload the game state. This could play well for Prometheus which has more of a "reset" idea than the others.
- Errors are something I find potentially interesting. You could imagine a linear story that ultimately tries to link to a passage that isn't there (which represents a completion state)? This might break the central idea of ultimately having something eternal though, unless there's some way to reset the experience after the error?
- Likewise an infinite loop could be funny, but again seems to give an ending which isn't desirable?
- Undo is an interesting idea as well? One could either trick the player into undoing their successful action (say pushing the boulder up a hill) or making it explicitly the only available action? Might be a bit contentious, though, to let them exist in a state that's finished.
- Timers (which are maybe built in? Maybe not?) are a way to cause something to happen, and that something could be a reversion of state? Most obviously a timer could be used to have the basin empty of water in Danaids, or have the eagle progress toward the player. But at that level it's really only serving a purpose much the same as any timer in other formats, so not very specific.
- Link repeating is intriguing perhaps especially for Zeno? The idea of a link that then reveals more text over and over again is an interesting way of representing the road travelled?
- Transitions might be a way to at least add some flavour?

## Designs?

### Sisyphus

- One of the tightly cyclical ones
- Could function as a cycling link or a cyclical graph for that reason
- Maybe cycling link as it feels more helpful here than in Danaids?

### Tantalus

- This most fundamentally for me seems to be about non-functional links? Perhaps this is where the error could be introduced? You can still go back away from the error perhaps?
- Either than or links that grey out and no longer work on mouse over? (Have to worry about mobile though in that case.) Maybe there could be a Reach followed by an Eat/Drink?

### Prometheus

- I like the idea of a save and restore? You could explicit say "game saves" in the first scene. Then the eagle arrives and eats your liver. And then the game restores back at the beginning literally. Quite nice. Do I want a big performance of needing to be able to struggle the eagle up? Is there any real advantage to representing this? Or better to have a linear telling? Weird given that struggling has been utterly central to my telling of the myth...?

### Danaids

- This feels the hardest as it often does, it's a more complex set of actions and involves transporting something from one place to another. I guess I can represent it with a variable saying whether you have the water or not, though you then end up with just kind of bad pseudo-parser IF?
- Still have cyclical graph "available" if I use cycling link for Sisyphus

### Zeno

- This feels like a candidate for the link-repeat idea? That each time you click you add distance to your progress but never actually get all the way there?

## And so...

Makes sense just to mock these up and see what we see I imagine?

---

# Reporting in on the full draft, single- versus multi-passage, reload?, done? (Wednesday, 26 June 2019, 15:19PM)

Well, I made mock-ups of them all as promised. Here is what happened.

## Sisyphus

I used the basic cycling link. There is no version of the link where the boulder reaches the top as that would create a (kind of) win state, so it's just "nearly there" followed immediately by "rolling down". It's the simplest of all the things I did and it's quite satisfying. Importantly it feels very Twiney. Kind of the ultimate Twiney thing, and a perfect fit here.

I went with very blank and sparse language which I think works fine. I mean, it just kind of works?

Little weird to feel like it might be "done" but who knows, perhaps it is.

Should I be doing the due dilligence of just playing a bunch of Twines to make sure I'm hitting the rough style and approach? Does that even make sense?

## Tantalus

This one was hard because I wanted to be fancy with mouse-overs, but have to acknowledge at the same time that it won't work with mobile. As such the base-line "trick" is that you click on links but they take you to pages where they turn out not to have worked, repeat ad nauseam. If using a mouse-style pointer this also happens on mouse over which is a little more fun and feels more like reaching, though I guess you could think of the movement as a reach and the click as a "grasp", in which case clicking is fine.

I spent a fair bit of time trying to get single-passage versions of this going with text and link replacement and so on, particularly liking the idea of things happening both on mouse over and mouse out. But again, if we're doing mobile that can't work anyway so perhaps not the biggest loss. (Not to mention I couldn't get it going anyway.) I think it's probably only to do with me wanting to flex my (non-existent) technical abilities, so also no loss there.

## Prometheus

I ended up doing this one just with timers and not with any save and load stuff. The save and load is pretty funny, but I suspect it's just more funny for me and not particularly visible on the surface for an actual player. Further, saving and reloading doesn't really register for me as a typical Twine experience kind of a thing, so I don't think there's enough of a hook into the "cultural practice" of Twine?

So the way it went is basically just a circular graph but with the transitions being based on timers. This is nice because the player has no agencies and just sees the cycle happening.

I ended up not implementing struggling because it just doesn't feel like it adds enough, just transforms it toward being more of a kind of systems/simulation experience, which Twine can do, but isn't really the kind of thing I'd say is typical or in its wheelhouse. As such the player does nothing except watch the eagle come and go.

## Danaids

The most systems-y one in a lot of ways (as seen with the text adventure). This is the one I "spent" the circular graph card on, so it's just four passages depicting the filling and emptying of the basin over and over again.

It maybe feels slightly less-than-ideal that two of the five are literal cyclical graphs, but on the other hand that really is the ultimate structure for a hypertext to represent repetition, so maybe it's acceptable. And I get brownie points for having the cycles be implemented differently and with different agencies right?

## Zeno

Relatively pleased that this one manages to "solve" the Zeno-representation problem in a very Twine-y way and also manages to do a single-passage thing (along with Sisyphus). In this case it's using text replacement stuff that allows you to have the agency of "I run" and to have that alter the representation of how far along the track you are. It uses "half of" repeating on itself to create the requisite distance-to-go infinitely which is nice given that halving just stacks neatly.

So I mean... is this thing somewhat... done?

## Single-passage versus multi-passage

I suppose this whole single-passage versus multi-passage thing does give us a particular aspect of Twine to think about. For me it currently feels most like a passage transition is a moment of action and time passing?

Or not? I don't know. Maybe the question is just an open one - what is the weighting and meaning of a textual/link change on the current page versus a transition to another page? What if the new page represents the exact same kind of textual/link change? Then the difference is just a light flicker? (At least with the default Twine passage transition.)

When I think about what I've seen in-page stuff done for (almost always cycling links) it has tended to be a way of altering flavour texts or expanding descriptive elements, so more about "looking" I suppose. Whereas in Sisyphus I'm using it to represent a very active piece of exertion. I think I "get away" with it here just because the cycling link is too good of a joke/play-on-commands in the context of Twine not to use. Anyone who has Twine-d will recognize what's going on and hopefully get a chuckle out of it. Which is part of the point of all this right?

## Reload?

One weird thing I noticed with Twine is that if you do a standard reload in the page (or select the location bar and hit enter) it won't reload back to the front page, which is maybe a little frustrating as it probably means 99% of people who even play will try one and get stuck in it and not bother to look at the others.

I guess I can see if there's a way to alter that behaviour, but I suspect it might be baked in there. And I really don't want to just offer an in-game "reload" as that would be admitting the punishments aren't infinite.

## World's fastest game?

So then have I finished one of these games in basically a day? Perhaps so, I don't think there's so much to agonize over here.

Show it to a person or two and call it a day? Perhaps so.

---

# A little extra note (Wednesday, 26 June 2019, 17:27PM)

Just to say I put the meta tag in for device font size stuff on mobile and it worked fine. All the things seem to be visible in a single screen now which is the ideal. Don't think it needs to be more than that.

May I say, too, that I quite love using the absolutely default CSS for Harlowe. Looks just so much like a... Twine.
