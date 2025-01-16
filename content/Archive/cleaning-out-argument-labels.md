---
title: "Cleaning Out Argument Labels"
date: "2016-12-02"
updated: 2023-03-26
categories:
  - "words"
---

The guys over at CleanCoders made a [video series on the creation of an iOS app](https://cleancoders.com/series/mobile-app-case-study). While refractoring, they decided to [remove keyword arguments](https://cleancoders.com/episode/mobile-app-case-study-episode-4).

> We also walked through the code replacing most of the keyword arguments with positional arguments – something that swift does not make particularly convenient. We did this because the code just _looked better_ once it was done.

I think this is a terrible idea.

Coincidentally, I’m in the middle of the chapter on function naming in [Clean Code](https://a.co/2qLr3ES). He argues against ternary arguments because it’s too easy to lose track of what arguments belong in the first, second, and third position. “Sounds like argument labels would help,” was my first thought. Looks like he disagrees. It makes me more skeptical of his other advice.
