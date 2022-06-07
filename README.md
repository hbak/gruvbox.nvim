# fork of ellisonleao/gruvbox.nvim with my own changes
don't use this fork, it's terrible and all decisions made out of anger
changes to be marked in code with comment "hbchange"

## 2022-06-06 can't ever tell where the fkn cursor is when searching
absolutely despise that I can't ever tell where the cursor is when doing hl search
- changing Cursor gui=reverse makes it so that you can change the cursor bg but you can't change the cursor fg on search results
### solution
- set a static fg and bg for Cursor, don't use reverse/inverse
- don't use gui=reverse for searches.   It's nice but cursor fg on search results will always be search bg, and that's too light to see against a white cursor
- use a dark color bg for search results.  Making fg darker helps it stand out more.   I set search bg = colors.faded_purple, fg = fg4


## initial changes
- shift dark[n] colors so that dark0_hard is the baseline, b/c there is a general reliance on each bg[n] to be slightly lighter than the previous.  Overlay screens were way too light.  Pmenu group changed, bg=bg1
- change bright_green to use springGreen from Kanagawa -- bc hate seeing an entire screen of puke green
		- TODO don't know if there's any differentiation between bright_green and bright_aqua
