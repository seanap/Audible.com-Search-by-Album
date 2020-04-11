# Audiobook Tag Scraper

This is a modified custom web source for [mp3tag](https://www.mp3tag.de/en/).  The original authors are qudo, dano, and Romano https://community.mp3tag.de/t/ws-audible-albums-and-series/41227 This helps me make sure all audibooks are Tagged properly, have the correct filenames, and have the proper folder structure.  This ensures consistency across Plex/Prologue, Booksonic, and other Audiobook Players.

Drop the `Audible.com#Search by Album.src` file in your `%appdata%\mp3tag\data\sources` folder

This script will set the following tags:

| mp3tag Tag    | Audible.com Value|
| ------------- | ---------------- |
| ALBUM         | Title            |
| SUBTITLE      | Subtitle         |
| YEAR          | Original Year*   |
| COMPOSER      | Narrator         |
| COMMENT       | Publisher's Summary|
| SERIES        | Series           |
| SERIES-PART   | Series Book #    |
| ALBUMSORT     | %series% %series-part% - %album%|
| COVER         | Cover Art        |
| ARTIST        | Author           |
| ALBUMARTIST   | Author           | 

*Audible is really bad at providing this data
   
## To Use:
Pull and set the tags: 
![alt text](https://i.imgur.com/AjJbUqE.png "Tag Source")
Set/fix the track numbers by hitting `ctrl-k`

Then set the filename and folder structure by clicking the Tag-Filename button: 
![alt text](https://i.imgur.com/KJGD4sE.png "Tag-Filename")

`Format String = %albumartist%\%series%\%year% - %album%\%album% (%year%) - pt$num(%track%,2)`  