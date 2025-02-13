## Building the gnAsteroid executable

<img src=/svg/space-rover-2.svg width=100 align=left style="padding-right: 25px;" alt="" />

1. clone gnAsteroid: `git clone https://github.com/gnAsteroid/gnAsteroid`
2. **Compile** with `go build -C cmd/ -o gnAsteroid`,
3. **Run** with `./gnAsteroid -asteroid-dir=example`, 
4. **Visit** the example with a browser at http://localhost:8888.

## Creating an asteroid

We built a `gnAsteroid` (or `gnAsteroid.exe` on Windows) file in the previous step. We will now create
an asteroid. Our first fictional asteroid will talk about someone called "bob".

To create an asteroid "bob", we create a directory `bob`, 
with these two simple files inside:

**bob/index.md**
```md
Hello the Gnosmos! This is [Bob](about.md)'s blog :)

Take a look at my [gnoface](/r/demo/art/gnoface:1337).
```

**bob/about.md**
```md
I'm Bob from Neptune. In a previous life, I was a sumo.
```

And that's it, we've created an asteroid with 2 pages. It's finished 😁.

The format is markdown. If you aren't yet familiar with it, it's extremely easy to learn.  Launch essentially like before:

`./gnAsteroid -asteroid-name "Bob's asteroid" -asteroid-dir bob`

And pay a visit to your machine's local TCP port 8888, that is http://localhost:8888.

<img src=/svg/telescope.svg hspace=10 width=100 align=left alt="" />

**Quiz**: if you noticed, this asteroid can render not only
`about.md` and `index.md` but a third page, namely a realm 
`/r/demo/art/gnoface:1337` hosted and run by validators on the gno.land chain but 
shown on your asteroid. Can you guess what the `:1337` is and what it does? 

<style type="text/css">
span.spoiler { color: gray; background-color: gray; }
span.spoiler:hover { color: initial; background-color: initial; }
html[data-theme=dark] span.spoiler:hover { color: gray; }
</style>

(**tip**: Using the asteroid, you can read the source of [/r/demo/art/gnoface/](r/demo/art/gnoface/) on-chain. **answer to the quiz**: <span class="spoiler">1337 is used as a parameter by realm /r/demo/art/gnoface. This will show the gnoface corresponding to that number.</span> **tip 2**: you can also see those realms [on gno.land](http://gno.land/r/demo/art/gnoface:1337), they are rendered by the same chain).


## Naming an asteroid

instead of specifying the name with `-asteroid-name <name>`, you may set it 
once in a file called `.TITLE` placed at the root of your asteroid. Only the first line will be read.

## Theming an asteroid

Asteroids are very rough rocks.

In the context of asteroids, we call **theme** a set 
of 3 folders: `css`, `font` and `img`. 

<style type="text/css">
img#really:hover { 
    content:url("/svg/chewbacca.svg"); 
}
</style>
<img id=really title="This does not use Javascript" src=/svg/darth-vader.svg hspace=10 width=100 align=left alt="" />

You may fork and modify the theme in `default-theme/`.  Then launch something like `gnAsteroid.exe -theme-dir=/path/to/your/theme -asteroid-dir=example`

Asteroids css are not standardized yet. Don't hesitate to just fork and experiment for now (and contribute).
## Editing

Editing an asteroid can be done with a simple text editor. Here are some [good editors](editors.md) which may work well with them.
## Publishing

Publishing your asteroid means to share it with other people. 

This is a work in progress, but [here's what works](publishing/) for now.

