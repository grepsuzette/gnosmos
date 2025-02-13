Here is a list of tested editors, and some notes about whether they work well to edit asteroids:

* **Obsidian** (**yes**, great, ubiquitous, free, but closed-source)
* LogSeq (maybe not)
* **vim** (**yes**, but technical)
* **Zettlr** (**yes**, great. Win, Linux, MacOs. Open-source)
* Joplin (no - uses a database)
* Roam research (no - uses a database)

### Obsidian

[Obsidian](https://obsidian.md/download) is perhaps the best graphical editor for asteroids.

Obsidian is ubiquitous (Windows, Mac, Linux, tabs and phones). Works great, looks great, options are great. The only drawback is it's not open-source.

![](fx/obsidian1.png)
Technically, its files are stored directly as files. So it's flat & selfless. We can open an asteroid directly and work on it. We can replace Obsidian with another editor. Reuse Obsidian again. It will always work. 

Notes:
- It adds a hidden `.obsidian/` folder which you thus should ignore in your sync process if your create one.
- Make sure to disable the option `Preferences / Options / Files and Links / Use [[ Wikilinks ]]` in order to use links like this: `[]()`
- You can create buttons to sync to a server (example a script with `rsync`. For instance say you have a script `x` containing `rsync -az ~/asteroids/myAsteroid/ 3.14.15.93:asteroids/myasteroid`, it can be launched with a sync icon using a very simple Obsidian plugin like [AlessandroRuggiero/script-launcher](https://github.com/AlessandroRuggiero/script-launcher). Plugins are also easy to write. Advise to [write your own plugin](https://docs.obsidian.md/Plugins/Getting+started/Build+a+plugin) based on the above, until there are some more trusted plugins in the community.

![Obsidian graph view of my asteroid](../fx/obsidian-graph.png)
<center><i>Obsidian can show graph view of yours asteroid in one click</i></center>

Apparently you can even install plugins like Excalidraw for drawing straight from within the software!

### vim 

 **Vim** and its ancestors have been used by admins and programmers for like half a century. gnAsteroid came to existence trying editing files served by gnoweb with [vimwiki](https://github.com/vimwiki/vimwiki) (a plugin). 

It works well with asteroids. But vim is very technical. And by no means a graphical solution. 
![vim with vimwiki's help](../fx/vimwiki.png)
 
Vimwiki is nice in that by clicking Enter on a word it will create a page, Enter on an existing page it will edit it, and Backspace will go back. Entering insert mode will unconceal the links, showing the file that is linked. But Vimwiki must be configured, and learned and it's such a rabbit hole; can not recommend this solution unless you are already a user and living in text interfaces is your thing. 
### LogSeq

[logseq](https://logseq.com/) is a popular editor, but it's not necessarily a great choice for editing asteroids. Every note is made of bullet points (an asteroid is made of regular markdown),

LogSeq is ideal for bullet journals, daily notes, and task management. It highly focuses on time and tags though and is block-based, not using flat files... 

Someone gotta try it, it's possible its philosophy pervades through your asteroid.
### Zettlr

https://www.zettlr.com/download

Zettlr is a great alternative to Obsidian, and it's Open-source. Available on Mac, Win, Linux, it has been growing on me. While especially targeting users who want to produce academic writing using Markdown (using LaTeX), it works great for simpler content such as asteroids. Obsidian and Zettlr are probably the two best choice at this time. You can edit an asteroid, and it won't leave byproducts there. Here is what it looks like: 

![](../fx/zettlr.png)

Notes:

1. Zettlr will use the `[[file]]` format (see the section at the end of this note) when you drag and drop a note inside another note. In Obsidian you can disable the `[[file]]` format, to retain the `[link](file)` used by gnoweb. Zettlr does not have this option.
2. Zettlr does not seem to recognize images located by absolute path compared to the root of the asteroid (Obsidian does), I had to use relative path e.g. `!(Map of Gnoland)[../fx/gnoland_map.png]`.   
3. Zettlr does not have plugins, therefore you can’t have a button to sync the files to your server/VPS to be served. You can still create a script manually though, or some clickable action through your OS menus (e.g. Shortcuts.app on MacOs).

Zettlr also have a **graph view**.

### Joplin

[Joplin](https://joplinapp.org) is a lovely open-source software. Unfortunately, its **markdown files are stored within a sqlite database**, rendering usage with gnAsteroid problematic.

For instance, it prevents simple synchronization methods, such as a straightforward usage of `rsync`. While it's always still possible to *export* the markdown files (even automatically, if we a plugin was used), this export operation is one-sided: when you edit a file thus exported, it won't affect the database within Joplin. Meaning using another editor like vim in parallel would *NOT* work.

*A fork of it [found in this thread](https://discourse.joplinapp.org/t/created-a-new-version-of-joplin-that-keeps-local-md-files/33339/45) is of interest: [Xilinota](https://github.com/XilinJia/Xilinota). But it's almost not used by anyone so we prefer not to recommend it.*
### Roam research

Roam Research uses a graph database to store its data, rather than traditional files. We can stop here... asteroids are file-based. A database won't work well.
### Others softwares

A lot of those are inactive:

* BoostNote: inactive since 2021
* TiddlyWiki: inactive since 2021
* Evernote?
