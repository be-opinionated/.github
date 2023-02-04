# Opinionated Development Drive

Welcome to the Opinionated Development Drive! This is an informal community for
helping projects migrate their tooling to be more opinionated about the things
that matter (and hopefully less opinionated about the things that don't).

## Why should my project be opinionated?

Opinionated tooling is often a good thing for developers. It helps to maintain
a consistent style, making reading easier, it helps find common issues, and
it helps people who are new to the project write code that will be accepted
upstream. All of these speed up development by taking things off the
developers' minds, allowing them to concentrate on what really matters:
producing high quality software.

## What shouldn't my project be opinionated about?

One of the hardest things about opinionated development is that it doesn't mean
"be opinionated about everything." In fact, many of the things about which
many developers are the most opinionated are some of the least productive
things about which to be opinionated. Does that mean you shouldn't have an
opinion on those topics? Absolutely not! You're welcome to have strong opinions
on all sorts of things, but the philosophy of opinionated development is about
when to assert an opinion and when the better answer is to "agree to disagree."

## When should I assert an opinion?

This is hard to say, and it varies from one project to the next. In general
though, asking yourself these questions can help you determine whether asserting
a particular opinion will be helpful:

1. **Is this going to make it easier for new people to contribute to my project?**
    
    This doesn't only apply to open source projects, either. Every project
    has a core team developing it. For some projects, that core team is a
    single person. For others, that core team may be dozens, hundreds, or even
    thousands of people spread across multiple continents. No matter what
    the project, consider that in the future, somebody else may end up helping.

2. **Is my project mature enough to care about this?**
    
    One of the biggest mistakes a developer can make is to spend more time
    worrying about tooling and consistency in a project than about the actual
    code. Technical debt is a difficult thing, because it's not always bad.
    If your choices are to create technical debt or never actually achieve the
    goal of a project, creating the technical debt is the obvious goal.
    With that in mind, don't scramble to spend time setting up tooling, standards,
    and all sorts of other requirements before making a program that does
    even the basics of what it sets out to do. As the [Zen of Python](https://peps.python.org/pep-0020/)
    states, "practicality beats purity."

3. **Does this actually affect code quality?**
    
    This can be very hard to examine, because it requires stepping away from
    one's preconceived notions. It's probably better explained with examples.

### Examples: When you *should* be opinionated

These are not hard and fast rules. However, here are some examples of times
when it's probably useful to be opinionated.

#### Indentation and other editor config

The [EditorConfig](https://editorconfig.org/) standard is a powerful standard
for helping your particular project tell a developer's editor how to handle
all sorts of things a developer shouldn't have to care about. This makes a
new contributor's life far easier because their editor can change its
configuration so things like newlines, tabs, and character sets are already
the way this particular project wants them.

Why is this important? Because fundamentally, the individual contributor's
opinion here doesn't matter. Spaces, tabs, indent size, line ends... You
might have opinions about them. But in the end, the most important thing to
do is "whatever this particular project does." Starting your own project?
Congrats! This is a rare case where you do get to push your opinion on others! 
But if you're contributing to a project, this is a case where the developer
(and their tools) being flexible and fitting with what the project decides
is going to be better than choosing not to contribute to a project because
they want three spaces rather than a single 8-character-wide tab.

Why should you implement editorconfig? Because while some people have strong
opinions, others just don't care. And either way, reconfiguring one's editor
for every individual project is more of a hindrance than a help. Letting
one's editor handle it is another thing a developer doesn't have to think about.

### Examples: When you *should not* be opinionated

This is often the hardest piece, and every one of these comes with exceptions.
But in general, there are times when being unopinionated is preferable.

#### Text editor wars — It's not worth it!

There are many strong opinions about what the best text editor, IDE, etc.
are. The author here even has his own strong opinions (opinions that will not
be shared). But fundamentally, the best editing environment is the one in which
the developer is comfortable. For the most part, this means you should keep
your project editor agnostic. Things like editorconfig (mentioned above) are
great ways to help with this. But this can also mean other things:

* Don't make your project dependent on one particular editor or IDE's tools
  (especially if this editor or IDE isn't available for all platforms, costs
  money, or otherwise has high barriers to entry)
* Don't encourage use of a particular editor for most projects

Of course, each of these has exceptions. If the project is, for example, a
plugin for a particular editor/IDE, it's perfectly reasonable to expect the
developers contributing to be using that software. It's probably even
preferable to encourage it while developing that plugin, as when the developer
is also an end user, bugs are often caught much earlier.

## How do I assert these opinions?

This is what the Opinionated Development Drive exists to enable! We intend to
create tools and processes to help with this, but at its core, the philosophy
is simple:

1. **Start with what's easy.** This means both that the tool should be easy to
    set up and that it should have general consent from existing developers.
    Consent doesn't necessarily mean agreement. It simply means everyone is
    willing to accept the standard. Existing standards that are simply being
    formalized with tools are often the best place to start.
2. **Do it progressively.** Small, frequent changes are better than large,
    infrequent ones. Setting up a new linter? Begin by enabling only rules
    that succeed on **all** of your code. "But everyone agrees this rule is a
    good thing and wants to change the code!" Great! **Do it later.** Don't
    worry, there are specific recommendations to help with that.
3. **Make atomic changes.** This is how you enable new rules that require code
    updates. Enable the rule, update the code, and submit just that and nothing
    else for review. Better yet, enable the new rules in one commit, update
    the code in another commit, and change the author on that commit to help
    future developers see that this is all the commit did.

## So... what's the process?

That's a work in progress!

# I disagree with this!

That's genuinely wonderful! Part of the purpose of this is to create a
consensus, not just push one set of opinions. File an issue. Start a discussion.
Make your opinion known, but be respectful while you do so. And above all,
please remember: the purpose of this community is not to put an end to 
discussions of what's a better way to do things, but rather to make these
discussions collaborative and useful.
