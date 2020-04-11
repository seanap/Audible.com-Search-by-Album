# Audiobook Tag Scraper

This is a modified custom web source for [mp3tag](https://www.mp3tag.de/en/).  The original authors are qudo, dano, and Romano https://community.mp3tag.de/t/ws-audible-albums-and-series/41227 This helps me make sure all audibooks are Tagged properly, have the correct filenames, and have the proper folder structure.  This ensures consistency across Plex/Prologue, Booksonic, and other Audiobook Players.

Drop the Audible.com#Search by Album.src file in your %appdata%\mp3tag\data\sources folder

This script will pull the following tags from Audible.com:

   Title = ALBUM  
   Subtitle of Album = SUBTITLE  
   Original Year* = YEAR  
   Narrator = COMPOSER  
   Publisher's Summary = COMMENT  
   Series Name = SERIES  
   Series Number = SERIES-PART  
   Cover Art = COVER  
   Author = ARTIST and ALBUMARTIST  
   ALBUMSORT = %series% %series-part% - %album%  

*Audible is really bad at providing this data
   
Once you pull and set the tags, then make sure the track numbers are set/fixed by hitting ctrl-k

Then set the filename and folder structure by clicking the Tag-Filename button and set
 
`Format String = %albumartist%\%series%\%year% - %album%\%album% (%year%) - pt$num(%track%,2)`