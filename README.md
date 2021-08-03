# ani-cli

This is a fork of Dink4n's [ani-cli](https://github.com/Dink4n/ani-cli) which itself is a fork of pystardust's [old-ani-cli](https://github.com/pystardust/ani-cli/tree/old-ani-cli). 

A cli to browse and watch anime.

This tool scrapes the site [gogoanime](https://gogoanime.vc).

## Usage

	# watch anime
	ani-cli <query>

	# download anime
	ani-cli -d <query>

	# resume watching anime
	ani-cli -H

	# settings
	ani-cli -s

Multiple episodes can be viewed/downloaded by giving the episode range like so

	Choose episode [1-13]: 1 6

This would open/download episodes 1 2 3 4 5 6

## Dependencies

* grep
* curl
* sed
* mpv
* awk
* fzf

## Optional Dependencies

* trackma
* dmenu

## Trackma 

While the original script was only meant to used to watch/download anime through terminal, this fork also uses [trackma](https://github.com/z411/trackma) to update your [Anilist](https://anilist.co/) as you continue watching the anime. So naturally, usage of this fork requires you to have anilist account and have that account added to trackma. Before using this script, there should be output of anime list when you enter `trackma -a 1 list` in ther terminal (where 1 is your Anilist account number). The anime you're trying to watch should also be added to your anilist for it to be updated. 

Note: Trackma account number 1 is hard-coded to the script. If the account number is different that that, it can be changed in the script at the top.

By default, trackma is not enabled. However, it can be toggled by changing the `use_trackma` variable to "yes" or "no".

## Dmenu

Dmenu can be used for various tasks like selecting anime, episodes etc or for choosing to update the show or not. By default, dmenu is not enabled. However, it can be toggled by changing the `dmenu` variable to "yes" or "no".
