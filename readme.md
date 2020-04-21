# Audiobook Tag Scraper

This is my modified custom web source for [mp3tag](https://www.mp3tag.de/en/).  The original authors are qudo, dano, and Romano https://community.mp3tag.de/t/ws-audible-albums-and-series/41227.

This script makes quick work of ensuring all audiobooks are tagged properly, have the correct filenames, and have the proper folder structure.  This ensures consistency across Plex/Prologue, Booksonic, and other audiobook players.

This script will set the following tags:

| mp3tag Tag    | Audible.com Value|
| ------------- | ---------------- |
| `TIT1` (CONTENTGROUP)  | Series, Book #   |
| `TIT2` (ALBUM)         | Title            |
| `TIT3` (SUBTITLE)      | Subtitle         |
| `TPE1` (ARTIST)        | Author, Narrator |
| `TPE2` (ALBUMARTIST)   | Author           |
| `TCOM` (COMPOSER)      | Narrator         |
| `TCON` (GENRE)         | Genre1/Genre2    |
| `TYER` (YEAR)          | Copyright Year*  |
| `COMM` (COMMENT)       | Publisher's Summary (MP3) |
| `desc` (DESCRIPTION)   | Publisher's Summary (M4B) |
| `TSOA` (ALBUMSORT)     | If ALBUM only, then %Title%<br>If ALBUM and SUBTITLE, then %Title% - %Subtitle%<br>If Series, then %Series% %Series-part% - %Title% |
| `TDRL` (RELEASETIME)   | Audiobook Release Year |
| `TPUB` (PUBLISHER)     | Publisher        |
| `TCOP` (COPYRIGHT)     | Copyright        |
| `ASIN` (ASIN)          | Amazon Standard Identification Number |
| `POPM` (RATING WMP)    | Audible Rating   |
| `WOAF` (WWWAUDIOFILE)  | Audible Album URL|
| `CoverUrl`             | Album Cover Art  |
| `TXXX` (SERIES)**      | Series           |
| `TXXX` (SERIES-PART)** | Series Book #    |
   >&ast;*I would prefer Original Pub. year, but Audible is really bad at providing this data*  
   >&ast;&ast;*Custom Tags used as placeholders, To view this tag Tools>Options>Tag Panel>New*  

## To Use:
1. Drop the `Audible.com#Search by Album.src` file in your `%appdata%\mp3tag\data\sources` folder.
2. Load Audiobook files, and select all tracks `Ctrl-a`
3. Set/fix the track numbers by hitting `Ctrl-k`
4. Click the Web Sources drop down button, select `Audible.com > Search by Album`
   ![alt text](https://i.imgur.com/Q4ySYh2.png "Web Source Select")
4. Then set the filename and folder structure by clicking the Tag-Filename button
![alt text](https://i.imgur.com/KJGD4sE.png "Tag-Filename")  
   `Format String = C:\path\to\Audiobooks\%albumartist%\%series%\%year% - %album%\%album% (%year%) - pt$num(%track%,2)`  
