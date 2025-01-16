---
title: "Markdown for Technical Documentation"
date: "2020-03-26"
updated: 2023-03-26
categories:
  - "words"
---

It seems like this advice comes along periodically: _Don’t use Markdown for technical documentation_. Hillel Wayne is the most recent plea to hit hacker news, but there have been others.

Hillel Wayne, [Please don’t write your documentation in Markdown](https://buttondown.com/hillelwayne/archive/please-dont-write-your-documentation-in-markdown/)

> Markdown cannot carry data. There’s no way to imbue properties into text using markdown. Good documentation is all about the semantic markup. A “definition” is not just a different formatting or like. It means there’s actually a concept of a “definition” as a discrete concept in your documentation.

Matthew Butterick, in [Pollen: the book is a program](https://docs.racket-lang.org/pollen/third-tutorial.html):

> Markdown is a limiting format for authors. Why? Because Markdown is merely shorthand notation for HTML tags. As such, it has three problems: it’s not semantic, it only covers a limited subset of HTML tags, and it can’t be extended by an author.

Eric Holscher, [Why You Shouldn’t Use “Markdown” for Documentation](https://www.ericholscher.com/blog/2016/mar/15/dont-use-markdown-for-technical-docs/)

> Though many people have added extensions to Markdown, almost none have any kind of semantic meaning. This means that you can’t write a Class or a Warning, you can only write text.

Mister Gold, [Stop Using Markdown For Documentation](https://web.archive.org/web/20200325160234/https://mister-gold.pro/posts/en/asciidoc-vs-markdown/)

> With Markdown you can only write text. It means that if you need to grab the reader’s attention with some kind of notes or tips, you have to embed HTML.

I have focused on the lack of semantic data in all these criticisms, because I think it is the most important drawback. The lack of semantic meaning in markdown makes in unsuitable for many technical writing tasks. Yet, I still write in markdown. This post is in markdown. There are a couple of reasons:

1. Its easy. I never forget the syntax. This may be because it is so limited, but it makes it easy to do simple documents.
2. It’s ubiquitous. The fact that there are so many different markdown parsers is not problem, its a strength. It’s usually trivial to add markdown to a system or workflow, regardless of the environment

What are the alternatives?

[ReStructurexText](https://docutils.sourceforge.io/docs/user/rst/quickstart.html) – If I were writing a book, I would probably use ReStructuredText. It is extensible, so you can add your own “roles”. But the syntax is pretty hard to remember. For example, here is the image syntax:

```
.. image:: images/biohazard.png
    :height: 100
    :width: 200
    :scale: 50
    :alt: alternate text
```

Of course, the benefit is that the image tag _has_ a height, width, and scale: something few markdown parsers support. It’s heavily tied to Python, which is something I’m comfortable with. It’s also heavily tied to a single implementation in [docutils](https://docutils.sourceforge.io).

[AsciiDoc](https://asciidoctor.org) – The syntax is more in the spirit of markdown. It seems to have coalesced around a Ruby implementation, and left the original [python implementation](https://asciidoc.org) languishing[\[1\]](#fn:1 "see footnote"). I was unhappy with the HTML produced by asciidoctor is styled entirely by `div` tags. Title ; just styles applied to named `div` tags.

[Pollen](https://docs.racket-lang.org/pollen/) – Very nice system. The fact it requires Racket is both admirable and a real-world pain. I gave up after trying to write my own pollen command. Trying to debug the unexpected return type from a nested [s-expresion](https://docs.racket-lang.org/plait/s-exp-tutorial.html) did me in.

For now, I stay with markdown, and all it’s shortcomings.

* * *

2. There are also two competing versions of aciidoc for python3: [asciidoc-py3](https://github.com/asciidoc/asciidoc-py3) and [asciidoc3](https://asciidoc3.org)  [↩](#fnref:1 "return to article")
