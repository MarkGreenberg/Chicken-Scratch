# Chicken-Scratch
Wolfram Language version of the 2-player educational game.

Chicken Scratch is a 2-player or 2-team educational game that is designed to be run by a teacher. The full game consists of: The Interface — one Wolfram notebook file that compiles into a .cdf (which can be played on the free CDFplayer); Question Modules — 225 Wolfram notebooks that deploy into cloud objects, each of which returns randomly generated questions for the game; and several hundred images for the interface and the questions.

To set up Chicken Scratch:

    NOTE: CS_ROOT is the folder in your Wolfram Cloud account where you are storing Chicken Scratch files. You can name the folder CS_ROOT whatever you want.
    
    1. Images — Copy the entire images/ subdirectory along with all its children files and folders to CS_ROOT. Every image needs to have permissions set to "Public".
    
    2. Interface — Copy CS_main02.nb to CS_ROOT, and then open it. Change the first line to urlStem="yourPath", where yourPath is the path to CS_ROOT. Execute the main block of code (urlStem="..." to newGame[]). You should see the interface appear as output. In the bottom block of code, change the function SetDirectory[] to point to the location where you want the Chicken Scratch .cdf to reside, not necessarily in CS_ROOT. Execute this bottom block of code (SetDirectory[...] to cdfFile=CDFDeploy[...]). It should create a .cdf file for Chicken Scratch's interface. NOTE: This will only work if you have an Enterprise license because Chicken Scratch uses dynamic content.
    
    3. Cloud Objects — There are 225 .nb files with names such as CS_packNB_Chem12.nb and CS_packNB_Lang4.nb. Copy all 225 of these into CS_ROOT. Open each notebook file. If it contains a file path reference, replace "XXXXX" with the path to CS_ROOT. (Most don't have a file path reference). Execute the code in each of these notebooks to produce a cloud object with a name like CS_packNB_Chem12 or CS_packNB_Lang4. At this point, Chicken Scratch should be ready to run.
    
To play Chicken Scratch:

    NOTE: Chicken Scratch is designed to be run by one person (HOST), typically a teacher, and played by two teams, typically consisting of 1-3 players each.
    
    1. Start — The interface starts with a title page (art and the words "Chicken Scratch"). Clicking anywhwere on the title page replaces it with the category view where a randomly chosen nine of the fifteen category names are displayed along with Grab Bag. Across the top are displayed the scores for both teams, a hand icon randomly pointing to the team that gets to go first, and the dollar value of the current question, which varies randomly from $24 to $96.
    
    2. Play — Clicking any of the categories brings up a randomly generated question in that category. Difficulty of the question is not tied to the dollar value. Choosing Grab Bag multiplies the dollar value by 1.5 and randomly picks from the nine displayed categories. The team whom the hand is pointing to indicates which of the four answers they choose. HOST clicks that answer. If it is right, then $$ is added to the team's score; if not, $$ is subtracted and the other team tries to answer for half the dollar value.
    
    3. End — The game automatically announces victory for the team whose score reaches $300 or whose opponent drops to -$300. There is a button beneath the interface to start a new game.
    
TIPS:

    1. HOST should read the questions aloud. This reinforces the player's exposure to academic language and provides a consistent rhythm to the game.
    
    2. To keep the game moving, give players a "reasonable amount of time" to answer. I usually give 15-30 seconds and then threaten to click on the wrong answer (which never happens).
    
    3. Many teachable moments arise during Chicken Scratch. Occassionally, before I click away from a question I'll give a very brief explanation of how I would answer. It is okay to show that you don't know all the answers. Be careful not to slow the game down too much.
    
    4. If the same players are going to play more than once, keep stats for a leader board. I record who is on the team, $$ earned, win/loss, and $$ gap over opponent.
    
    5. Chicken Scratch works well for tournaments. I use a single- or double-elminiation bracket over several days for tournaments.
