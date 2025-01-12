+++
title = "Note Taking with Emacs and Org Roam"
author = ["Shiva Tamil Kumaran"]
date = 2025-01-12T15:18:00+00:00
tags = ["emacs", "org"]
categories = ["computing"]
draft = false
+++

I've recently started working on my master's thesis, and as such I've been looking for a
good way to take notes. I need to be able to capture notes on my reading, as well as any
ideas or thoughts that I have. I've previously experimented with:

-   **Notion** - I did like how feature rich it was, but I disliked the rigid organisation
    structure. I felt forced to organise everything into a heirarchical pages and sub-pages.
    Also, it felt like once I committed to _Notion_, it wouldn't be possible to switch
    platforms if I wanted to.

-   **Obsidian** - Based on my issues with _Notion_, it would seem like this is the answer.
    I liked the [zettlekasten](https://zettelkasten.de/introduction/) approach to note taking - it felt more unstructured
    and aligned better with how ideas and thoughts naturally arise. I also really liked the
    idea of all my notes being stored locally as text files. It seemed like the perfect
    solution... until I saw the power of _Emacs_ and _Org._


## Why Org? {#why-org}

I was drawn to how extensible it is - the ability to completely customise a workflow to match
your exact purposes is unmatched. I was also drawn to the rich set of features it supports, whilst
still being based entirely on text. I don't think I'll do the best job of selling
just how amazing this seemingly simplistic piece of software is, but there is a lot of discourse
regarding this topic on the internet already.


## Setting up A Zettlekasten with Org Roam {#setting-up-a-zettlekasten-with-org-roam}

<a id="figure--roam-graph"></a>

{{< figure src="/images/roam-graph.png" caption="<span class=\"figure-number\">Figure 1: </span>Graph view of my notes so far" >}}

[Org roam](https://www.orgroam.com) is an extension of org mode, which facilitates "networked thought", similar to tools like
_Roam Research_ or _Obsidian._ The key feature of this extension is the ability to seamlessly link
together org files. It also indexes this network of files, allowing to quickly search and jump
between these files. Lastly, it surfaces _backlinks_, which are references
to the current file inside other files. The idea is that these backlinks give contextual
information and help you easily traverse your network of thoughts.

<a id="figure--roam-preview"></a>

{{< figure src="/images/roam-preview.png" caption="<span class=\"figure-number\">Figure 2: </span>An example note, showcasing inline LaTeX rendering, and backlinks" >}}

Out of the box, it is already a very useful tool. I've been using it to build up a sort of
second brain - I use it to capture most of the thoughts I have, about any topic.
It pairs brilliantly with org mode's organisational and task tracking features (which I may cover
in a future blog post).


### Capturing Thoughts {#capturing-thoughts}

_Org roam_ ships with an excellent feature, called _dailies_. These are daily notes which you can
easily capture to with a convenient keybinding:

<a id="figure--roam-daily"></a>

{{< figure src="/images/roam-daily.gif" caption="<span class=\"figure-number\">Figure 3: </span>Capturing a daily note" >}}

I use this to capture incomplete thoughts and ideas as they come up, and hopefully flesh them out into
fully fledged entries in the zettlekasten. I can flag these ideas that I want to revisit with the `IDEA` keyword
I also use _dailies_ to maintain journal - it is quite interesting to look back on past entries!


### Processing Captured Thoughts {#processing-captured-thoughts}

I then search for anything flagged with the `IDEA` keyword through org mode's in-built agenda feature.
This has been a very useful feature - it means that I actually action ideas I have, rather than forgetting
about them, or making a note which I never revisit.


### Bibliography Management {#bibliography-management}

As an example of how extensible org mode is, let's explore how I've integrated
bibliography / citation management into my note taking workflow.
[This article](https://www.riccardopinosio.com/blog/posts/zotero_notes_article) gives much more detail on how to set this up. You can also have a look at
my [dotfiles](https://github.com/shiva-tk/dots) for more details.


#### Zotero {#zotero}

[Zotero](https://www.zotero.org) is a bibliography management tool. Using a browser extension, I can save research papers
to my library with a single click. Using the _better bibtex_ extension for zotero, I have set up
an automatic export of this library to _bibtex_.


#### Citations in Org Mode {#citations-in-org-mode}

Using this bibtex file, I can easily insert a citation for any paper in my library:

<a id="figure--org-cite-insert"></a>

{{< figure src="/images/org-cite.gif" caption="<span class=\"figure-number\">Figure 4: </span>Inserting a citation" >}}

I can also quickly open up a paper from my library which I've referenced in a note:

<a id="figure--org-cite-open"></a>

{{< figure src="/images/org-cite-open.gif" caption="<span class=\"figure-number\">Figure 5: </span>Opening a referenced paper" >}}


## And More... {#and-more-dot-dot-dot}

This is just a taste of what's possible. In future posts I may cover how I track tasks
with org mode.
