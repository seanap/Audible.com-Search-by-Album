This is a modified custom web source for mp3tag.  The original authors are qudo, dano, and Romano https://community.mp3tag.de/t/ws-audible-albums-and-series/41227 

Drop this file in your %appdata%\mp3tag\data\sources folder

This script will pull the following tags from Audible.com:

Title = ALBUM
Subtitle of Album = SUBTITLE
Original Year = YEAR
Narrator = COMPOSER
Publisher's Summary = COMMENT
Series Name = SERIES
Series Number = SERIES-PART
Author = ARTIST and ALBUMARTIST
ALBUMSORT = %series% %series-part% - %album%

Once you pull and set the tags, make sure the track numbers are set/fixed by hitting ctrl-k

Then set the filename and folder structure by clicking the Tag-Filename button and set the Format String = %albumartist%\%series%\%year% - %album%\%album% (%year%) - pt$num(%track%,2)