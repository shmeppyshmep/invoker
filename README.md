# Invoker
A command line Bandcamp download tool to simplify the process of downloading owned releases to your server. 

This is very basic for now with only one command 'invoke'. It is setup in simple bash and uses `wget` & `unzip`.

## Installation

1. Clone or copy the invoker file to your local or server
2. Make sure to set permissions on the invoker file: `chmod 755 invoke`

## Usage

1. Login to you Bandcamp account, find the release you want to download and follow the download link to the download page.
2. Select which format (FLAC, MP3 etc) from the dropdown and wait for the download link to be prepared
3. Once the download link is prepared right click the download button and copy the source URL to the clipboard
4. Go to the command line and type `./invoker invoke PASTED_URL DESTINATION_FOLDER`

This will trigger `wget` to download the file to a temporary zip, it will then be unzipped to the destination folder specified at the end of the invoke command

Example below:

`./invoker invoke 'http://p4.bcbits.com/download/album/album_hash/mp3-v0/xxxxx?id=AAAAA&sig=BBBBB&sitem_id=XXXXXX&token=YYYY' 'Shmeppy - Funky as I wanna be (2016) [FLAC]'`

## Notes
It's a good idea to wrap the pasted download source URL into single or double quotation marks, same with the source destination folder name.

After running invoker you can also jump into the folder and cleanup the file names using a simple `rename` command. This is because Bandcamp tends to put the artist name and album name into the file names to. This is personal preference though.

 