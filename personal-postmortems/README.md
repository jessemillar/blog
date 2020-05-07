# Personal Postmortems

[![Work In Progress Tombstone GIF](header.gif)](https://giphy.com/stickers/wip-work-in-progress-eani13-hS9x8qV9bCrBBHx2rq)

I've had great success in using personal postmortem documents when trying to learn from a failure (big or small). I found a simple postmortem template that I liked and spun up a public repo (public inside my company) to host all my docs. At the end of projects/sprints/individual feature development, I write a postmortem and share it out with the team. Sharing helps me be accountable, foster a culture that accepts failure at varying levels, and inspires other people to also self-examine and learn as much as possible from their individual experiences.

The general template is shown below:

```
#

## Summary


## What Didn't Go Well

-

## What Went Well

-

## Results

-

## Appendix

### Links

- []()

### Timeline

- []
```

I also made a [long-form template with inline tips and examples](template.md).

## Fun Tip

If you use [Neovim](https://github.com/neovim/neovim) or similar, you can save [the simplified template I included above](https://github.com/jessemillar/dotfiles/blob/master/neovim/.templates/postmortem.md) as a file and then put something like this snippet in your `.vimrc` file to automatically load the template anytime you create a new file prefixed with `postmortem-`:

```
au BufNewFile postmortem-*.md 0r ~/.templates/postmortem.md
```

Be sure to specify the correct save location for the template file. I have a segment of [my dotfiles](https://github.com/jessemillar/dotfiles) that automatically puts a few useful templates in `~/.templates`.
