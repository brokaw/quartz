---
title: "Ulysses vs. iA Writer"
date: "2019-07-07"
updated: 2023-03-26
categories:
  - "words"
---

I’ve been looking for a serious writing program. Maybe _serious_ isn’t the right word, because I use Vim and BBEdit, and those are nothing if not serious. But they don’t feel right for the type of concentrated, long-form prose that I am trying to write. The contenders that I settled on are iA Writer and Ulysses.

Both are great, and I would recommend either. Choosing between them is more about your personal preferences, workflow, and writing needs. My observations based on my particular needs are below.

You should also check out the comparison by [Marius Masalar](https://mariusmasalar.me/in-search-of-the-perfect-writing-environment-ia-writer-vs-ulysses-358c95d07bd5/).

## Comparison

This is not comprehensive, just a few things that happen to be important to me.

### Post to Wordpress

Ulysses posts to self-hosted Wordpress installations.

iA Writer requires Jetpack for self-hosted Wordpress.

I have no desire to install Jetpack, so this is a drawback to iA Writer. Ulysses works exactly the way I want it to.

**Update**: Starting with [iA Writer 5.5](https://ia.net/topics/new-pdf-preview-better-web-publishing-improved-editing), Wordpress posting on personal sites [has been improved](https://steven.brokaw.org/posts/ulysses-vs-ia-writer).

### File Management

iA Writer works on files. Ulysses works on “sheets,” a file abstraction that lives in a database owned by the application.

Both approaches have their advantages. iA Writer’s advantages:

- The files are **searchable with Spotlight**. Using Finder to search for things will reveal your iA Writer files just as well as searching within iA Writer.
- The files are **portable**. It is easy and immediate to edit the files in another program. I can use BBEdit or Vim to open a file I created in iA Writer without having to export.
- I can keep the files in a **git repository**. iCloud probably serves most writers’ needs, but if you’re a git user, having your history in a repository is reassuring.

The downside is that I am doing my own file management. I have to decide what to name a new document. I have to decide where to save my file. These little decisions can slow me down.

By contrast, Ulysses works with a container that manages the files for me. The benefit of this is that no file name or folder location is required when I create a file (or “sheet”). Just ⌘N and I’m ready to write.

It also easy to compose a work of many sheets. It lets me think in sentences and paragraphs instead of files. I can combine sheets, rearrange their order, “glue” sheets together, and split them apart. It’s more flexible and useful than iA Writer’s “content blocks.”

### Fonts and Appearance

Ulysses has a very detailed preference pane to customize every element of my Markdown syntax. I can create themes, and I can use themes created by others. Ulysses comes with a solarized theme, so I picked that. Then I noticed that there is another solarized theme: slightly different and more in line with what markdown looks in MacVim. So I changed to that. After a while, that started to feel garish, so I switched to a theme that mimics Editorial. This was great. But now that theme is starting to look a little…I don’t know…too subdued, maybe. I’ll find something I like if I keep looking. If not, there’s a way to create custom theme styles…

iA Writer looks great. There is a setting for light or dark. There is a font setting with three choices. I picked the one I like and haven’t given it much thought since. I feel none of the theme malaise that Ulysses makes me feel.

### Markdown

iA Writer is straight markdown, more or less. More textual than Ulysses, anyway. That is, a link in iA Writer looks exactly like you would expect:

```
[Link anchor text](https://example.com/path/to/target.html)
```

Ulysses has clever little additions that make it less textual and more graphical. The target URL is not listed in the source view. If you double-click on the link text, a little inspector window opens to show the target link. It’s very well done, but I feel the textual nature of markdown is a benefit, and Ulysses loses that.

### Share Extension

Ulysses has a (poor) Safari share icon. It can paste a web site title and URL, and that’s about it. It is no match for Bear or Keep It.

iA Writer has no service or share extension.

## (Preliminary) Decision

I like iA Writer better. Even though Ulysses does have real advantages, iA Writer just _feels_ better. I like the fonts and the built-in preview styles. I like the more standard, textual markdown source. I like the options for previewing the rendered markdown.

The file handling goes both ways. I can totally get behind Ulysses’ philosophy, but I like having my content indexed in Spotlight.

I love that Ulysses can post directly to my WordPress blog. I get around this iA Writer deficiency by using Byword to open the file created by iA Writer and posting from there. This workaround may become tiresome, but for now it works.

This comes down largely to aesthetics and intangible preferences.

## Potential Game Changers

These are things that might tip my decision the other way, after more time using them.

- WordPress posting. Ulysses just does WordPress posting the way I want.
- File management. I can see myself coming to prefer Ulysses’ style after a spending more time with both.
- Writing Goals. Ulysses can track writing goals, both daily, and set per sheet.

## Non-issues

iA Writer has a feature that will highlight words based on parts of speech (nouns, verbs, etc.). I don’t find this useful.

Many are outraged by the subscription pricing of Ulysses. It doesn’t bother me. It is useful how a single subscription gives me access to macOS and iOS versions of the app. If I start writing more with my my iPad, this might be useful.

## Recommendation

My recommendation is that you can’t decide, get both. You can get a week’s trial of both. If that isn’t enough time, just buy iA Writer, and buy a monthly subscription to Ulysses. Give yourself a couple of months to settle into them both. One will reveal itself as your favorite.

This is what I’m doing. I prefer iA Writer, but Ulysses has clear advantages. I want to live with both and see which feels better over the long term. There might be drawbacks to iA Writer that get annoying only over time. When I make a final decision, I’ll post an update.
