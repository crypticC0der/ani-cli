# ani-cli

This is a fork of Dink4n's [ani-cli](https://github.com/Dink4n/ani-cli) which itself is a fork of pystardust's [old-ani-cli](https://github.com/pystardust/ani-cli/tree/old-ani-cli).

A cli to browse and watch anime.

This tool scrapes the site [gogoanime](https://gogoanime.vc).

## Usage

	# watch anime
	ani-cli <query>

	# download anime
	ani-cli -D <query>

	# resume watching anime
	ani-cli -H

	# settings
	ani-cli -s

	# player
	ani-cli -p <player>

	# toggle trackma
	ani-cli -t <0/1>

	# toggle dmenu
	ani-cli -d <0/1>

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

While the original script was only meant to used to watch/download anime through terminal, this fork also uses [trackma](https://github.com/z411/trackma) to update your [Anilist](https://anilist.co/) as you continue watching the anime. In order to use it, you'll need an anilist account and have that account added to trackma. Your currently watching anime list should be the output when you enter `trackma -a 1 list` in the terminal (where 1 is your Anilist account number). The anime you're trying to watch should also be added to your anilist for it to be updated.

Note: Trackma account number 1 is hard-coded to the script. If the account number is different that that, it can be changed in the script at the top.

By default, trackma is enabled. However, it can be toggled by changing the `use_trackma` variable to "yes" or "no" in the script or by using flag `-t 1` to enable and `-t 0` to disable usage of trackma.

## Dmenu

Dmenu can be used for various tasks like selecting anime, episodes etc or for choosing to update the show or not. By default, dmenu is not enabled. However, it can be toggled by changing the `dmenu` variable to "yes" or "no" in the script or by using flag `-d 1` to enable and `-d 0` to disable usage of dmenu.
