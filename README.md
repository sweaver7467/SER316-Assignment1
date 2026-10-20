README


BRANCH STRUCTURE with LINE CHANGES + Current branch changes
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