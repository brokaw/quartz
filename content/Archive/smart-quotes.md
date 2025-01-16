---
title: "Smart Quotes"
date: "2016-12-31"
updated: 2023-03-26
categories:
  - "words"
---

Via [Daring Fireball](https://daringfireball.net/linked/2016/12/29/fleishman-curly-quotes), Glenn Fleishman’s [Atlantic article on curly quotes](https://www.theatlantic.com/technology/archive/2016/12/quotation-mark-wars/511766/):

> The trouble with being a former typesetter is that every day online is a new adventure in torture. Take the shape of quotation marks. These humble symbols are a dagger in my eye when a straight, or typewriter-style, pair appears in the midst of what is often otherwise typographic beauty. It’s a small, infuriating difference: "this" versus “this.”

I write my content in Markdown, render it to HTML, and post raw HTML into WordPress. It’s a couple extra steps, but I get to write in a proper text application, and the output is reliable and well-formed. During that process the quotes are “educated” to transfrom plain ASCII inch marks to proper double quotes.

Ironically, the quote above is the biggest problem I’ve encountered in a while: the plain quotes are automatically educated, so I have to update the HTML output and change it back. Then I discovered that [WordPress automatically educates my quotes](https://codex.wordpress.org/Function_Reference/wptexturize), so I couldn’t display straight quotes even though I wanted to. I would have to update WordPress to remove the `wptexture` filter. I started this post explaining how easy this was for me, but only proved the point that it is a pain purposely using both proper quotes and dumb straight quotes. Using one or the other is easy.
