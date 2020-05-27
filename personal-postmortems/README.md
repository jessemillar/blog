# Personal Postmortems

[![Work In Progress Tombstone GIF](header.gif)](https://giphy.com/stickers/wip-work-in-progress-eani13-hS9x8qV9bCrBBHx2rq)

People are lazy. Let's just get that out of the way. *Because* people are lazy, if we want to improve, we need some structure and accountability. Postmortem documentation is a great way to help a team learn and be accountable. To expand the team benefits of postmortems, I've modified software postmortem processes to be more personal and focused on individual growth.

Before we dive into what a personal postmortem is, let's lay some groundwork. Software developers are cute and like to use (*cough* steal *cough*) fun terminology. Outside the software world, [a postmortem](https://en.wikipedia.org/wiki/Autopsy) is a synonym for "autopsy" which means cutting open dead people to figure out how they died.

> The term "post-mortem" derives from the Latin for post, meaning "after" and mortem meaning "death". The principal aims of an autopsy is to determine the cause of death, mode of death, manner of death, the state of health of the person before he or she died, and whether any medical diagnosis and treatment before death was appropriate.

In software land, we treat our code as a person and pretend that person died whenever there was an issue. What happened that caused last week's software outage? Could we have done anything to prevent it? Did we have proper monitoring in place to know that something was broken or dead before our customers discovered the rotting skeleton in our closet?

[Postmortem discussions](https://en.wikipedia.org/wiki/Postmortem_documentation) usually happen at the end of a project. The team usually sits down together, goes over what was successful and unsuccessful about the project.

Project post-mortems are intended to inform process improvements which mitigate future risks and to promote iterative best practices. Post-mortems are often considered a key component of, and ongoing precursor to, effective risk management.[2]

TODO Talk about why we benefit from modifying the structure to be more personal

Like dissecting cadavers, personal postmortems aren't for the faint of heart. Writing and sharing a personal postmortem doc takes some serious effort, reflection, and humility. Sure, you can write a postmortem doc and keep it to yourself in some folder on your desktop. That's still a solid step above not doing any self reflection. But, to get the full benefit of personal postmortems, you need to share the final doc with your team.

I've had great success in using personal postmortem documents when trying to learn from a failure (big or small). I found a simple postmortem template that I liked and spun up a public repo (public inside my company) to host all my docs. At the end of projects/sprints/individual feature development, I write a postmortem and share it out with the team. Sharing helps me be accountable, foster a culture that accepts failure at varying levels, and inspires other people to also self-examine and learn as much as possible from their individual experiences.

I find it difficult when writing a postmortem to highlight positives. Remember as you write that a postmortem doc is just as much about celebrating successes and lessons learned as it is about identifying shortcomings and potential growth areas.

Looking back on completed projects/tasks is an important thing to do if you want to improve. This repo exists to track semi-raw (meaning that enough detail is present to prevent posting to a public GitHub repo) postmortems for projects I've worked on at Microsoft.

It's important to note that postmortems do not need to be limited to when things go wrong. The whole point is to reflect on your experience to maximize your learning and then share that newfound knowledge with your team. A postmortem discussing a conference you attended or a feature you added is just as relevant as one discussing the time you brought down production.

Modeling vulnerability by openly sharing your shortcomings and challenges leads to more rapid personal progress and a healthier team culture. If everyone on your team feels comfortable with experimentation and learning from potential failure, there will be more collaboration, better discussion, and healthier code.

## Template

This repo includes [a template file](template.md) that can be used for writing your own retrospectives. The template is simple and can be expanded if needed, but remember and apply the guiding principle of [Bullet Journaling](https://bulletjournal.com/): Keep things simple enough that you don't feel overwhelmed or demotivated. The point is to get things on the page.

The general template filled with explanations is shown below ([and available as a separate file](template-demo.md):

```
# (Put a Catchy Title Here)

## Summary

Write a brief, one-paragraph summary of what happened/what you worked on. Put enough detail that someone can skim and quickly understand what's going on but don't bog things down with technical details or griping. Try to be objective. When referencing yourself, either speak in the third person or make it very clear who wrote the document. "I" or "me" might not make sense to someone else later on.

## What Didn't Go Well

Give an overview of what didn't go well. Use a list for better readability. If things really didn't go well, it's natural to have negative emotions, but don't use this section to rant. Look at data and facts. Don't be afraid to mention people by name, but try not to throw people under the bus. Examples below.

- I overpromised and didn't deliver the feature on time
- I got in an argument with a teammate which ended up being silly because we were actually on the same page
- I'm not entirely proud of the code I ended up writing (lost of "here be dragons" comments)

## What Went Well

For this section, format similarly to the "What Didn't Go Well" section, but instead talk about the things that *did* go well. Don't try to use this section to override or hedge the "What Didn't Go Well" section. Be objective, factual, and aware of your latent emotions. Loose examples follow. Be specific in your actual postmortem.

- I learned a lot about a new technology
- We have a more defined PR process in place
- I added a lot of explanatory comments to our code

## Results

Make a list of lessons you learned and what you're going to do differently in the future. Also list (and link to if possible) any files, documents, etc. that came about as a result of whatever your postmortem is discussing. Bullets are your friend here.

- I should be more realistic in the future when deciding how much work I can take on in a set amount of time. It would have been better if I'd only promised to deliver parts X and Y before the end of the month instead of also including Z.
- Our documentation could use some improvement and it doesn't take much effort. I was able to create [a new onboarding page]() with links to six other pages to help our interns get up to speed.
- [A not-yet-closed PR]() that still needs a couple reviews.
- [A new web page]() explaining the feature to our customers.

## Appendix

All appendix sections are optional and should only be included if relevant.

### Links

Put a list of relevant links here for easy reference. Some generic examples are shown below.

- [A link to a PR discussion]()
- [A wiki page outlining a design or timeline]()
- [A web page outlining a conference you went to]()

### Timeline

Fill this section with a list of timestamps showing what happened in what order. In most cases, you likely won't need to be more granular than a day, but make sure you include the year for future readers.

- [4/15/2020] I was given the task and started researching
- [4/16/2020] I pair programmed with someone
- [4/21/2020] I fought with a technology
- [4/23/2020] I created the final PR
```

Once you're comfortable with the general idea of the sections, here's [a minimal template](template.md) for quickly filling out postmortems.

## Fun Tip

If you use [Neovim](https://github.com/neovim/neovim) or similar, you can save [the simplified template I included above](template.md) as a file and then put something like this snippet in your `.vimrc` file to automatically load the template anytime you create a new file prefixed with `postmortem-`:

```
au BufNewFile postmortem-*.md 0r ~/.templates/postmortem.md
```

Be sure to specify the correct save location for the template file. I have a segment of [my dotfiles](https://github.com/jessemillar/dotfiles) that automatically puts a few useful templates in `~/.templates`.

## Notes

There is some debate over whether to call these "postmortems", "retrospectives", etc. I've kept this repo titled "Postmortems" for two reasons:
1. Regardless of "correctness", "postmortems" is the term you see most in industry and quickly conveys the purpose
1. I initially named the repo "Postmortems", discovered the point of debate, and am too lazy to rename the repo

