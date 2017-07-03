# pouetboy
<h3>Gather audio from https://pouet.audio</h3>

<h3>Install:</h3>

<h4>Make the script executable (ie, 'chmod +x pouetboy')</h4>
<h4>Use the script by yourself:</h4>
+ Copy the script into one of the PATH component (eg, /usr/bin/local, /usr/bin/, etc..)
<h4>Use the script as an automated task:</h4>
+ Edit your crontab file to schedule the script call, with 'crontab -e':

<pre>
PATH=/home/duke/bin
HOME=/home/duke/bin
0 */2 * * * pouetboy
</pre>
        
Then it should do its job every 2 hours in that case, telling you the result by email:
<pre>
Date: Mon,  3 Jul 2017 10:04:02 +0200 (CEST)

-- Existing Database pouet-audio.sqlite (loaded: 217 files)
-- Looking on https://pouet.audio
++ 6 new audio files
++ Cerrone - Supernature (Official Video)             (3:52) @ https://m.youtube.com/watch?v=QgGK4qBTwpw 
++ Stevie Ray Vaughan - Tin Pan Alley (aka Roughest Place In Town) - Live At Montreux85 (13:07) @ https://www.youtube.com/watch?v=RfhLbmUGKb8&list=WL&index=1 
++ Becca Krueger Cover of Ray Charles Hit the Road Jack (4:40) @ https://www.youtube.com/watch?v=OfUDsHtSv88 
-- executed in 240 s
</pre>
        
<h3>Usage:</h3>

<pre>
$ pouetboy -h
Usage: pouetboy [options]

Options:
  -h, --help            show this help message and exit
  -d DIRECTORY, --directory=DIRECTORY
                        Working directory
  -f DATABASE, --filename=DATABASE
                        Database file name
  -b URLBASE, --base=URLBASE
                        Source URL
  -l, --list            List actual database according to arguments
  -v, --verbose         Print out every new file (even skipped ones)
</pre>

<h3>Example:</h3>

<pre>
Date: Mon,  3 Jul 2017 10:04:02 +0200 (CEST)

-- Existing Database pouet-audio.sqlite (loaded: 217 files)
-- Looking on https://pouet.audio
++ 6 new audio files
++ Cerrone - Supernature (Official Video)             (3:52) @ https://m.youtube.com/watch?v=QgGK4qBTwpw 
++ Stevie Ray Vaughan - Tin Pan Alley (aka Roughest Place In Town) - Live At Montreux85 (13:07) @ https://www.youtube.com/watch?v=RfhLbmUGKb8&list=WL&index=1 
++ Becca Krueger Cover of Ray Charles Hit the Road Jack (4:40) @ https://www.youtube.com/watch?v=OfUDsHtSv88 
-- executed in 240 s

</pre>
