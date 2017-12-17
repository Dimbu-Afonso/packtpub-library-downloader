# PacktPub Library Downloader

Automatically download all your eBooks and videos. (See: [PacktPub Free Daily Book](https://www.packtpub.com/packt/offers/free-learning))


## How to use it:
	python downloader.py -e <email> -p <password> [-d <directory> -b <book assets> -v <video assets>]

##### Example: Download books in PDF and EPUB formats and accompanying source code
	python downloader.py -e hello@world.com -p p@ssw0rd -d ~/Desktop/packt -b pdf,epub,code

##### Example: Download videos, their cover image, and accompanying source code
	python downloader.py -e hello@world.com -p p@ssw0rd -d ~/Desktop/packt -v video,cover,code

##### Example: Download everything
	python downloader.py -e hello@world.com -p p@ssw0rd -d ~/Desktop/packt -b pdf,epub,mobi,cover,code,details -v video,cover,code


## Commandline Options
- *-e*, *--email* = Your login email
- *-p*, *--password* = Your login password
- *-d*, *--directory* = Directory to download into. Default is "packtpub_media/" in the current directory
- *-v*, *--videos* = Assets to download. Options are: *video,cover,code*
- *-b*, *--books* = Assets to download. Options are: *pdf,mobi,epub,cover,code,details*

**Video Asset Options**

- *video*: The video file
- *cover*: Cover image
- *code*: Accompanying source code

**Book Asset Options**

- *pdf*: PDF format
- *mobi*: MOBI format
- *epub*: EPUB format
- *cover*: Cover image
- *code*: Accompanying source code
- *details*: Creates a JSON file with the title, # of pages, and description. (slows downloads)


## Dependencies:


* [Requests](http://docs.python-requests.org/en/latest/) for HTTP requests:

		pip install requests

* [lxml](http://lxml.de/) for HTML parsing:

		pip install lxml

Tested working on Python 2.7.11 and Python 3.6.0 :: Anaconda 4.3.0 (64-bit)
