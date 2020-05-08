# Personal Postmortems

[![Work In Progress Tombstone GIF](header.gif)](https://giphy.com/stickers/wip-work-in-progress-eani13-hS9x8qV9bCrBBHx2rq)

People are lazy. Let's just get that out of the way. Heck. I'm lazy. I've been putting off this post for a long while.

*Because* people are lazy, if we want to improve, we need some structure and accountability.

TODO Talk about what a general postmortem is
TODO Talk about why we benefit from modifying the structure to be more personal
TODO Write and post a few more personal postmortems so I have more experience to draw from

This post isn't for the faint of heart. Doing this takes some serious effort, reflection, and humility. Sure, you can write a postmortem doc and keep it to yourself in some folder on your desktop. That's still a solid step above not doing any self reflection. To get the full benefit of personal postmortems though, you need to share the final doc with your team.

I've had great success in using personal postmortem documents when trying to learn from a failure (big or small). I found a simple postmortem template that I liked and spun up a public repo (public inside my company) to host all my docs. At the end of projects/sprints/individual feature development, I write a postmortem and share it out with the team. Sharing helps me be accountable, foster a culture that accepts failure at varying levels, and inspires other people to also self-examine and learn as much as possible from their individual experiences.

## Overview

Looking back on completed projects/tasks is an important thing to do if you want to improve. This repo exists to track semi-raw (meaning that enough detail is present to prevent posting to a public GitHub repo) postmortems for projects I've worked on at Microsoft.

It's important to note that postmortems do not need to be limited to when things go wrong. The whole point is to reflect on your experience to maximize your learning and then share that newfound knowledge with your team. A postmortem discussing a conference you attended or a feature you added is just as relevant as one discussing the time you brought down production.

Modeling vulnerability by openly sharing your shortcomings and challenges leads to more rapid personal progress and a healthier team culture. If everyone on your team feels comfortable with experimentation and learning from potential failure, there will be more collaboration, better discussion, and healthier code.

## Template

This repo includes [a template file](template.md) that can be used for writing your own retrospectives. The template is simple and can be expanded if needed, but remember and apply the guiding principle of [Bullet Journaling](https://bulletjournal.com/): Keep things simple enough that you don't feel overwhelmed or demotivated. The point is to get things on the page.

## Notes

There is some debate over whether to call these "postmortems", "retrospectives", etc. I've kept this repo titled "Postmortems" for two reasons:
1. Regardless of "correctness", "postmortems" is the term you see most in industry and quickly conveys the purpose
1. I initially named the repo "Postmortems", discovered the point of debate, and am too lazy to rename the repo

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
