## What to write
Based on: [Writing Great Documentation Series](https://jacobian.org/series/great-documentation/)


It's like a story or martial art, there are continuous flow, basic explanation for concepts, and there is tension (story) or pressure test (martial art)

### Step by step AKA tutorial & Getting Started
Good tutorials are a must as they’re usually the first thing someone sees when trying out a new piece of tech. First impressions are incredibly important: that rush of success as you work through a good tutorial will likely color your future opinions about the project.

### Overviews & Topical guides
This is the meat of your documentation. Once somebody’s learned (from a tutorial) the high-level concepts, they’re going to need to dive into the details of some area or another. Any documentation worth its salt is going to have a whole bunch of these.

The main goal for topical coverage should be **comprehensiveness**.

### Low-level, deep dive reference material
Finally, you need complete reference for all the public APIs your project provides. These should be designed for those who already know _how_ to use some API, but need to look up the exact arguments some function takes, or how a particular setting influences behavior, etc.


## Technical style
### Learn to write
Unfortunately, there aren’t any shortcuts here. The best way to learn how to write great documentation is to first _learn how to write_ (anything). There are some important differences between technical documentation and your average prose, but a solid foundation of good written communication skills is an irreplaceable prerequisite.

So how do you learn to write (anything) well? There’s only one answer: you’ll learn to write well if you write. A lot.

You’ll probably want to balance out all this writing with a healthy dose of reading, too. Learn to identify the mechanical parts of what makes a piece of writing effective; try to identify what succeeds (and what fails) about everything you read.

### Grammar
- Strunk and White's The Elements of Style
- Diana Hacker's A Pocket Style Manual
- Handbook of Technical Writing

### Style
Chicago Manual, MLA, and APA.

In the end, though, it really doesn’t make a whole lot of difference. The important lesson from all this is to _be consistent_. Readers find different stylistic choices off-putting, and they lend an uneven, unfinished tone to the documentation. Choose a stylebook, learn it, and then follow it… sometimes.

### Good documentation style
##### Markup
There’s one huge difference between the way people read print and the way they read electrons: when people read online, they skim. Study after study has shown that readers skip a large percentage of the words that float by on their computer screens.

This means that good online documentation will feature a much heavier reliance on markup than most style guides allow for. In practice, this means:
- Use inline markup liberally
- Write in short paragraphs
- Use a variety of structural elements
  lists, tables, code block and the like. Callout.
- Make your structure visual
  Header is necessary. Avoid pointless transitions. Stop skimmers as they fly by down by page. Headlines help reader quickly find the section of the document they're looking for.

##### Style
- Be conversational.
  Write in a tone similar to how you talk. This doesn’t mean including all those verbal tics (“well…”, “you see”, “um…"), and it doesn’t mean throwing grammar rules out the window. If you use “gonna” in a technical document I’m “gonna” hate you.
  
  But it _does_ mean that contractions are okay, as is starting sentences with conjunctions.

- Don't be afraid to strike a personal tone.
  You probably learned never to use “I” in a formal essay. Well, I’m here to tell you that it’s just fine in technical work. Showing your personal voice helps readers identify with the material, and that makes the material less intimidating.
  
  You _do_ need to be careful to be consistent with pronouns in collaborative works. You might choose to always use “I,” even in works written by different authors. Leonard Richardson and Sam Ruby took this path in [RESTful Web services](https://www.amazon.com/dp/0596529260/?tag=jacobian-20). Or you might choose to use “we”, even in parts written by a single author. Adrian and I went this way in the [Django book](http://djangobook.com/). As long as you’re consistent, either approach works.
  
- Do be careful with tenses and persons.
  Most documentation, and especially tutorials, is written in the second person, future tense. That’s stuff like “first, you’ll need to install FooBar version 7. Then, when you’ve frozzled the whizbang, you can start working on the doodad.” This is the general form I prefer since documentation is essentially instructional material and I like the conceit that I’m personally instructing my readers.
  
  Another common form is to couch everything in the first person plural: “first, we’ll need to install FooBar version 7…” This has advantages: it implies that the author is right there in the thick of things with the reader. But it can lead to confusion if later the author wants to be more conversational.
  
  Once again there’s no “correct” way here, but you’ll want to think about this question, figure out a standard, and stick to it.
  
- Watch out for passivity.
  You’ve probably learned to avoid passive voice in your writing. That’s usually good advice, but it’s not the whole story; what I mean here is that good technical writing is active. The verb always appears first. Remember: you’re instructing people, so make it clear what to _do_ at all times.
  
  To illustrate, my first draft of the above paragraph started, “your high school English class probably taught you that passive voice was bad style.” That’s not passive voice (”… English class… taught…” is plenty active), but it _does_ obscure the actual action in question – what “you… learned”. Starting the sentence with “you learned” brings the focus back onto _you_, the reader, hence keeping with the conversational, instructional tone I’m trying to strike.
  
- Omit fluff.
  This is best illustrated by example. Yesterday’s piece contained this ugly sentence:
  >This means that it should be pretty cross-sectional; a good tutorial should show off most of the different areas of the project.
  
  A commenter (rightly) took me to task for this one: this sentence has a number of words (“pretty”, “most”, “good”) that don’t add any meaning to the sentence and some others (“different areas”, “the project”) that are vague.
  
  Here’s a better version:
  >This means that it should be cross-sectional; a tutorial should show off the major areas of your project.
  
  The meaning’s the same, but the second version is more forceful, clearer, and shorter. This is good.
  
- Watch out for written tics.
  Everyone’s got certain bad habits when it comes to writing. I think of these as written tics: little habits that have become nearly involuntary. Once you notice a writer’s tics it’s hard to stop noticing. The repetition just gets in the way.
  
  For the record, my written tics are an over-reliance on semicolons and em-dashes; this document contains far too many – of each.

## You need an editor
### Self editing
- Avoid editing and writing simultaneously. Nothing kills flow worse than continuously second-guessing yourself. So turn off spell-check, turn off grammar checks, and most importantly try to turn off the critical part of your mind until it’s time for editing.
   
   This is one of the major reasons I end up at a coffee shop or library for editing: I write something, print it out, and the walk over to edit it somewhere else. I’m trying to train myself into thinking of editing as a totally separate role I’m performing that doesn’t even happen in the same place I write.
   
- Give it some time. If you let some time pass between writing and editing, then what you’ve written will fade a bit from your memory and start to appear a little less familiar. You’ll be less likely to “know” that you got something write, and a little more likely to catch errors.
  
- Change your margins. This is a really silly trick, but damn does it work. Just change column width or margins in your editor, and when your text reflows it’ll look slightly different. I find that this little difference is enough to jog my brain awake, and I often find things I’ve missed right away after a reflow.
