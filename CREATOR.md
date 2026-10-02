# A note from the creator

My name is M. Arslan. I'm a computer science student from Lahore,
Pakistan, and I built Ghosthread AI on my own, part-time, over the
last several months.

This page is here because the project doesn't belong to a company. It
belongs to one Architect. If you're reading the documentation and you
want to know who wrote it, who is behind it, and why it exists — this
is that page.

---

## Why I built it

Every automation tool for Windows asks for the same thing:

*Stop what you're doing and watch me work.*

I hated that. I wanted to keep typing while a script ran. I wanted my
cursor to stay where I left it. I wanted a tool that behaved like a
second pair of hands working quietly alongside me, not a program that
took over my screen the moment it started.

Nothing on the market did that. AutoHotkey was brittle and script-based.
Browser tools stayed in the browser. Cloud workflow tools streamed my
files to someone else's servers. And the new wave of AI assistants all
lived in a chat window on the side, waiting to be asked.

So I asked a different question: *what if automation never asked for
your attention at all?*

The answer turned out to be a different way of talking to Windows —
one where actions are delivered directly into each app's own message
queue instead of being simulated on the screen. That's what Ghosthread
is built on. Everything else in the project is a consequence of that
one idea.

## What I'm proud of

Three things, in order:

**The privacy posture.** Ghosthread is local-first by design, not by
marketing. Your files, screens, memories, and preferences stay on your
machine. When the software needs cloud reasoning for a complex task, a
privacy filter scrubs paths, keys, and identifiers before anything
leaves your device. Air-Gap mode disables cloud access entirely. This
is the thing I care about most, and I may not compromise on it.

**The safety model.** The software assumes the AI can be wrong. Its
safety boundaries are enforced at the deepest layer of the application,
beneath the reasoning model, in a way the AI cannot argue around. The
system cannot write to Windows system folders. It cannot permanently
delete your files. It refuses to operate in games and anti-cheat
sessions. These are not rules the AI agrees to follow. They are
physical stops it runs against.

**The idea.** Whether or not you think the software is polished, or
ready, or trustworthy, I hope you can see that the underlying idea is
a good one. Automation that runs off-screen is a different category of
tool than automation that runs on-screen. I think it's the right
category.

## What I'm honest about

This is a solo project. It's in beta. 
There are bugs. Documentation may lag behind the code. Response times 
for issues and emails vary, because there is one person on the other 
end, and that person also has a life too.

I'd rather tell you that plainly than pretend otherwise.

## Where I want this to go

I want Ghosthread to have a real user base — a thousand people, then
ten thousand, using it every day and telling me what's broken and what
should change. Free through that phase. I want it to earn a place in
the industry as a serious tool, built by someone who took privacy and
safety seriously from the first line of code.

And yes — I want people who find this project to find *me* too.
If you're reading this and you think I did something worth doing,
that's the whole return on the work. You can reach me at any of the
links below.

## Reach me

- **Email:** ghosthreadai@gmail.com
- **X:** [@ghosthreadai](https://x.com/ghosthreadai)
- **Instagram:** [@ghosthreadai](https://www.instagram.com/ghosthreadai)
- **Facebook:** [Ghosthread AI Official](https://www.facebook.com/profile.php?id=61594822401353)
- **Website:** https://ghosthread.online
- **Personal GitHub:** [github.com/ghosthread-ai] 

I read every message.

— **Architect: M. Arslan**