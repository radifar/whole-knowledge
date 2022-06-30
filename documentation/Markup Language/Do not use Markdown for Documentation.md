https://ericholscher.com/blog/2016/mar/15/dont-use-markdown-for-technical-docs/

### Lack of a standard
Commonmark was developed to solve this problem

### Flavors

### Lack of Extensibility
With other markup languages, you can extend the language to provide the features that you need. They have mechanisms in the syntax to add new functionality, without breaking from the original spec and creating a new language.

reStructuredText for example, has both inline and block level markup:

```rst
.. contents:: All the stuff I'm going to talk about
   :depth: 2

Please look at :rfc:`1984` for more information.
This is implemented in our codebase at :class:`Example.Encryption`.
```

You can learn more about the [rfc](http://docutils.sourceforge.net/docs/ref/rst/roles.html#rfc-reference), [class](http://www.sphinx-doc.org/en/stable/domains.html?highlight=domains#cross-referencing-python-objects), and [contents](http://docutils.sourceforge.net/docs/ref/rst/directives.html#table-of-contents) concepts.

As a developer working with rST or Asciidoctor, I can add new markup to the language in a simple, pluggable way. I don’t have to change how the language is parsed, and I can share those additions with other users via a standard extension mechanism.

**There is no way of doing this in Markdown, in a way that would be portable across versions.**

### Lack of Semantic Meaning
Though many people have added extensions to Markdown, almost none have any kind of semantic meaning. This means that you can’t write a _Class_ or a _Warning_, you can only write text.

This leads people to embed HTML directly in their Markdown:
```html
<div class="warning">

This is a Warning!

</div>
```

In reStructuredText for example, you can write:
```rst
.. warning:: This is a Warning!
```

This will be output as a warning properly in HTML, PDF, and any other output format you can generate.

**Semantic markup firmly separates the words that you write from how they are displayed.**

Writing without semantic markup is a problem for a few reasons:

-   Your Markdown is now dependent on specific CSS classes in your display, meaning your writers have to think about how your page will be designed
-   Your content is no longer portable to other output formats (PDF, etc.)
-   Conversion to other markup tools and page designs becomes much harder


### Lock In and Lack of Portability
The explosion of flavors and lack of semantic meaning leads to lock in. Once you’ve built out a large set of Markdown documents, it’s quite hard to migrate them to another tool, even if that tool claims to support Markdown! You have a large set of custom HTML classes and weird flavor extensions that won’t work anywhere but the current set of tools and designs.

You also can’t migrate Markdown easily to another markup language (Asciidoc or RST), because Pandoc and other conversion tools won’t support your flavor’s extensions.

I think that a lot of people choose Markdown because they think they can migrate to another tool or markup later. Markdown is definitely the lowest common denominator, except that for any reasonably sized set of docs you’ll need things that aren’t in the basic language.

**Once you start using markdown flavors, which is required for any non-trivial documentation, you lose all portability benefits.**