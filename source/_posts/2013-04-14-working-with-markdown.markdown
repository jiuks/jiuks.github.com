---
layout: post
title: "Working with Markdown"
date: 2013-04-14 23:18
comments: true
categories: [Markdown, Productivity]
---
Over the last year I have been becoming more and more reliant on [Markdown][markdown]. Pretty much everything I write is in [Markdown][markdown], most my writing starts in [nvALT][nvalt], whether this is notes from meetings, emails, or anything longer I could be writing.

## Writing

As an editor [nvALT][nvalt] does a good job, however for anything that is longer than a few hundred words I normally use a dedicated editor. Depending on the nature of what I am writing I would say my top three are: [TextMate][textmate],  [Folding Text][foldingtext] and [iA Writer][iawriter]. [TextMate][textmate] I like because of the autocompletion on the Escape Key, so if I am writing quite a technical document which has a lot of repeated words then it seems the quickest way of writing.

<!-- more -->

[Folding Text][foldingtext] I like for outlining, planning out larger pieces of work and writing presentations. I also like the UI, so some of the longer things I write are done here. I think I'm right in saying that [Folding Text][foldingtext] doesn't implement OSX's autocorrect when typing, which I find quite useful, maybe a better typist wouldn't need it.

[iA Writer][iawriter] has the simplest and hence most productive interface. I like to use this in full screen mode when I just want to get my head down and write.

Other things I have tried are [Byword][byword], [Multi-Markdown Composer][multimarkdowncomposer] and recently [Ulysses III][ulysses]. [Byword][byword] I feel I should like, however have just never got enough traction with. [Multi-Markdown Composer][multimarkdowncomposer] I get, but just don't find writing on it that easy and I haven't quite got the stylesheets set up correctly yet. [Ulysses III][ulysses] to be honest I just don't get. I saw a couple of good reviews for it, but it really doesn't work for me.

## Previewing

[nvALT][nvalt] also has a build it preview window that can be brought up by a key command, this is useful for quick previews, however the best tool I have found for previewing is [Brett Terpstra's][brettterpstra] [Marked][marked]. This is just quick and easy, plus you can use different styles including a [GitHub][github] one.

To preview an more advanced [Markdown][markdown] or [Multi-Markdown][multimarkdown] [Marked][marked] is required.

It should also be noted that [Multi-Markdown Composer][multimarkdowncomposer] uses a two pane approach, so you write and edit on the left and it previews on the right.

## Additional Tools and Services

[TextExpander][textexpander] is one of the first things I install on any Mac or iOS device and I have started to build up a library of [Markdown][markdown] related snippets. There are also some good libraries available online from [MacSparky][macsparkysnippets] and [Brett Terpstra][btsnippets], who also has some specific [iOS ones][btiossnippets].

[Brett Terpstra][brettterpstra] has also built a set of [Markdown Service Tools][markdownservicetools] which give you a load of accelerators and shortcuts for writing Markdown. The one I found the most useful was [SearchLink][searchlink] which is a quick way to put placeholder links when writing a page and then service will go and serach the internet and complete all the links.

## Consuming and Publishing 

So that pretty much covers off the writing side of things, the next step is where any of this gets published to. Let's start with the easy stuff. The majority of what are notes that are consumed by me, so I use [nvALT][nvalt] and [Dropbox][dropbox] to make sure everything is synced between my two laptops, iPhone and iPad. [nvALT][nvalt] has very good search and I would strongly recommend using tags.

We also use [GitHub][github] a lot at [Rittman Mead][rittmanmead], [GitHub][github] supports [Markdown][markdown], so that is pretty easy. It also goes without saying that [Octopress][octopress] publishes [Markdown][markdown] natively, so, again, that is easy.

We also have a [Wordpress][wordpress] [blog at Rittman Mead][rmblog], plus we use [Zendesk][zendesk] as a knowledge base internally. Both these sites allow you to write posts in HTML, so I generally preview the document in [Marked][marked] and then copy the HTML to the clipboard.

### Email

Quite often I will want to email what I have written. I have three approaches here:

1. Convert the note into a PDF, or possibly Word, document and send as an attachment.
2. Open up [Gmail][gmail] in [Chrome][chrome], compose or reply to a mail and paste in my [Markdown][markdown] note and use a plugin called [Markdown Here][markdownhere] to convert the note to rich text.
3. Use OSX's Mail.app to send the mail, paste in the [Markdown][markdown] and use one of the [Markdown Service Tools][markdownservicetools] to convert it to rich text.

For short notes, it seems a bit of an overkill to convert everything to a document and attach it so I tend to use (2) or (3) most regularly. [Markdown Here][markdownhere] seems to provides a much better rendering  of the note, so aesthetically that is my preference, however it breaks my workflow, I generally prefer an email client to a browser and despite trying many different email clients, when I am using OSX I tend to find using the native apps win out, so that means I use Mail.app and Safari most regularly. I find that pretty much another other tool that converts [Markdown][markdown] to Rich Text tends to use Heading 1 sizes that look way too big and some [Multi-Markdown][multimarkdown] features can easily be lost.

I can't say I really have this figured out, however I can work around it. Ideally I would like a keyboard shortcut to take a [nvATL][nvalt] note and create a new Mail.app message with something like [GitHub][github] formatting.

## Challenges

Anything more complicated than this I am still having challenges with, and am looking for ways to really solve the problem.

### Commercial Documents

I write quite a lot of commercial documents at [Rittman Mead][rittmanmead], in the form of proposals, statements of work and commercial/legal agreements. I will often draft these in [Markdown][markdown], ideally I want to then press a button, use a keyboard combination or even run a script and these will be output to a formatted PDF document.

I believe all documents a company outputs should be a high quality. Previously I used Pages and [Word][word] for this. I could write fairly well formatted in Pages and the export to PDF function gave a true rendering of the Pages document. The main problem I had with this was that:

* I much preferred writing in [Markdown][markdown];
* I wanted to separate the content from the formatting, so if we changed our look and feel, or if the proposal needed to be written from the US office this was regeneration, not re-authoring;
* there is not a seamless integration of Pages between iOS and OSX, whereas there is for text files.
* Pages files, despite how good [Spotlight][spotlight] is, don't have the same ease of search as text files in [nvATL][nvalt].

### Formatted Output

Currently my best approach to this problem is to us a command line utility called [Pandoc][pandoc] which is a multipurpose converter that happens to take [Markdown][markdown] as an input and you can select various outputs such as PDF, [ePub][epub] or [Word][word].

The reason I started using [Pandoc][pandoc] was because when I exported to PDF from [Marked][marked] I found it followed more of a web page paradigm, so there was:

* no concept of pages, just one long PDF document;
* no way to have headers and footers in the document. I would typically use these to contain the company logo, a document reference, date and page numbers.

[Pandoc][pandoc] gave me this ability, however the [Markdown][markdown] to PDF conversion uses [LaTex][latex]. This means I had to learn a bit of [LaTex][latex] to be able to create the formatting, headers and footers that I needed and also the document has a bit of a [LaTex][latex] look and feel to it.

One quite major issue I had with [Pandoc][pandoc] was using tables in the [Markdown][markdown]. [Pandoc][pandoc] didn't ever wrap the text, so if you had a table with a lot of text in, it just disappeared of the side of the page. This was a pretty big problem for me.

### Word

My use of [Word][word] was solely driven by clients requiring to review and red line commercial and legal documents using Word's [Track Changes][trackchanges] feature. I am sure a large proportion of sales of the cash cow that is Microsoft Office is driven by corporate needs like this.

[Pandoc][pandoc] also does a pretty good job of generating [Word][word] documents, and even has the option to base the formatting on another [Word][word] document, where it will pick up the Heading 1, Normal and other common styles from the template document.

## Collaboration

I also need to write collaboratively. [Google Docs][googledocs] is excellent for this allowing for real time multi-user editing, however provides absolutely no support for [Markdown][markdown] and I really struggled getting [Markdown][markdown] documents formatted and uploaded to [Google Docs][googledocs].

My current best approach is to create private [Gists][gists] and share the URL with other collaborators. [Gists][gists] can be written in [Markdown][markdown] and [GitHub][github] offers a great diff utility that I find far easier to read than [Word's][word] [Track Changes][trackchanges]. This approach is asynchronous, as opposed to [Google Docs'][googledocs] real time, synchronous editing.

I recently read about [Draft][draft] and have signed up for an account, but have yet to try it in anger.

## Next Steps

The real challenge I have is to get well formatted PDFs from [Markdown][markdown] to do this I will either continue looking at [Pandoc][pandoc] and [LaTex][latex], however I think I may have reached the limits here, without changing the type of [Markdown][markdown] I write, or start to look at customising the CSS previews for [Marked][marked], though I have no idea if things like headers and footers will be possible. I do seem to remember that the PDF export from [Byword][byword] was a multi page PDF, so that at least must be possible.

### Source Control

One final idea I'm thinking about at the moment is to create a [GitHub][github] repository out of the directory where all my text ([Markdown][markdown]) files are kept. Although [Dropbox][dropbox] does a great job of syncing files and keeps an incremental history of every save, I'm thinking the ability to checkpoint files could be useful. One thing I don't know however is how well [Dropbox][dropbox] and [GitHub][github] play together.

## To Conclude

I now use [Markdown][markdown] to write everything, or at least everything I write starts out as [Markdown][markdown]. Where the output can be in [Markdown][markdown] or HTML then this works amazingly well. However where my workflow requires a more complex output, or I need to collaborate with others, then there are still a few challenges to resolve before the process is seamless.

It should also be noted that there is a growing number of resources available to augment writing in [Markdown][markdown], some of which I have mentioned above. Using [Markdown][markdown] and these resources has significantly improved my productivity and made writing far more enjoyable.


[markdown]: http://daringfireball.net/projects/markdown/
[nvalt]: http://brettterpstra.com/projects/nvalt/
[textmate]: http://macromates.com/
[foldingtext]: http://www.foldingtext.com/
[iawriter]: http://www.iawriter.com/mac/
[byword]: http://bywordapp.com/
[multimarkdowncomposer]: http://multimarkdown.com/
[ulysses]: http://www.ulyssesapp.com/
[brettterpstra]: http://brettterpstra.com/
[marked]: http://markedapp.com
[github]: https://github.com
[multimarkdown]: http://fletcherpenney.net/multimarkdown/
[textexpander]: http://smilesoftware.com/TextExpander/index.html
[macsparkysnippets]: http://macsparky.com/tesnippets/
[drdrang]: http://www.leancrew.com/all-this/2012/07/markdown-reference-links-from-safari-tabs/
[btsnippets]: http://brettterpstra.com/projects/te-tools/
[btiossnippets]: http://brettterpstra.com/2011/02/17/markdown-snippets-for-textexpander-on-ios/
[markdownservicetools]: http://brettterpstra.com/projects/markdown-service-tools/
[searchlink]: http://brettterpstra.com/projects/searchlink/
[dropbox]: http://www.dropbox.com/
[rittmanmead]: http://www.rittmanmead.com/
[rmblog]: http://www.rittmanmead.com/blog/
[wordpress]: http://www.wordpress.com/
[zendesk]: http://www.zendesk.com/
[chrome]: https://www.google.com/intl/en_uk/chrome/browser/
[draft]: https://draftin.com/
[gmail]: https://mail.google.com/
[markdownhere]: https://chrome.google.com/webstore/detail/markdown-here/elifhakcjgalahccnjkneoccemfahfoa/related
[octopress]: http://octopress.org/
[spotlight]: http://en.wikipedia.org/wiki/Spotlight_(software)
[word]: http://office.microsoft.com/en-gb/word/
[trackchanges]: http://office.microsoft.com/en-gb/word-help/track-changes-HA102840151.aspx
[pandoc]: http://johnmacfarlane.net/pandoc/
[epub]: http://en.wikipedia.org/wiki/EPUB
[latex]: http://www.latex-project.org/
[googledocs]: http://docs.google.com/?hl=en
[draft]: https://draftin.com/
[gists]: https://gist.github.com/