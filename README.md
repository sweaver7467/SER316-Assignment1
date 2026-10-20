README

AFTER PART 2:

Merge involves combining branches and resolving any potential resolutions, which also maintains each branch's commit history. This 
strategy is likely to be the safest method of applying 
changes, but it is best when the desired target branch is merged into 
the changed branch to resolve conflicts first.

Rebasing is similar to merge, except that it rearranges a commit to be 
a direct descendent from the desired rebase target. This is useful for 
maintaining clean, linear history. This strategy would best be used 
when working locally before a push is made and could affect others, and
to create a cleaner commit history than merging.

Squash is practically a "rebase in-place" in the sense that it clears up
history, but does not alter its working tree. I think this strategy 
would best be used when having to return to working on a branch after 
making a commit to save work, but the newest snapshot is a more complete
version - and is better reflected on a final commit. Like the example,
only the "done" commit should be carried forward since it is complete.

Cherry-pick was not very well covered, but seems to fill a need for a
copy-paste action, rather than a full merge or rebase so that other 
branches are left unaffected. I also noticed that it appears clean in 
commit history. This strategy might be best as a half-step of a rebase,
where the changes are brought to be the direct descendent of a branch,
without deleting the branch (or commit) it was pulled from like a 
rebase would.

I have been working on this for a while and encountered several things 
I had to look up. I don't remember much about what I observed in the
git history between features. Feature 1 was simple and straightforward.
Feature 2 had multiple resolutions, and when it was done it looked crazy.
After feature 3 was complete, squashing was done, the history looked 
pretty clean.


INITIAL BRANCH STRUCTURE with LINE CHANGES + Current branch changes
main	Engine	60
|	    UI	22
|	    Guess	49
|	    Main	15
|	    Util	21
|
|------ documentation no lines affected
|       1 commit (ammended from updating this)
|       Desc:   This document
|
|
|------	feature1	Engine	73\*	
|	    4 commits	UI	22
|	        		Guess	49
|	        		Main	32\*	
|	        		Util	21
|
|	    Desc:		Quit ability
|       			Play again loop
|       			Feedback for guesses
|
|
|------	dev		    Engine	60
|	    | 1 commit	UI	    22
|	    |		    Guess	49
|	    |		    Main	16\*	
|	    |	    	Util	21
|   	|
|   	| Desc:		User encouragement message
|   	|
|   	|
|	    |------	feature2	Engine	82\*	
|	        	2 commits	UI	    22
|			            	Guess	49
|			            	Main	16
|			            	Util	21
|
|		Desc:		Implement max attempts, game over
|
|
|------	feature3	Engine	90\*	
|	    4 commits	UI	    22
|		        	Guess	49
|		        	Main	15
|		        	Util	21
|
|	    Desc:		Implement hint giving
|
|
|------	hotfix		Engine	60
|	    1 commit	UI	    22
|		        	Guess	49
|		        	Main	15
|		        	Util	21
|
|	    Desc:		bug fix