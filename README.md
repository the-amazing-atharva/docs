# Fiberplane Docs

All main Fiberplane Docs are available here as markdown files. To see the rendered preview navigate to our documentation website [docs.fiberplane.com](https://docs.fiberplane.com/docs)

## Editing guide

We use [ReadMe](https://readme.com/) to render our documentations site and host our markdown that we upload through a Github action workflow.

### Page setup - YAML frontmatter

ReadMe sets up the right categories in the sidebar and the right links using the frontmatter at the top of the documentation.

The basic format is:

```yaml
---
title: Title of your new page
category: <category_id> # the category under which it should be nested
slug: cli # the slug for the cli
---
```

### Adding links to other docs pages

There are also some nuances when adding links. Instead of the normal markdown relative links `[linked text](./relative/link)` we need to use the following format:

```markdown
[linked text](doc:the-slug-of-the-linked-piece)
```
To add links, replace `linked text` with the text that you want to display as the link, and `the-slug-of-the-linked-piece` with the slug of the piece that you want to link to. 

#### For Example :
If you have a file called `getting-started.md` and want to link to it from your `README.md` file, you could use:
```markdown
[Getting started](doc:getting-started)
```
**Note :**
When using this format for links in your documentation, make sure that the `slug` matches the actual *filename* or *header* of the piece you are linking to. You can also use this format for linking to other sections within the same document.

Using this format ensures that your links are compatible with your documentation tool, and allows users to easily navigate between different pieces of the documentation.
