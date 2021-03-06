# fakemenot
Python CLI app to detect if a screenshot of a tweet is genuine. Work in Progress.

### Requriements

* tesseract
* tesseract-data-eng

### Setting Up
* Install `tesseract` and `tesseract-data-eng` packages.

  * Ubuntu (and other debian based) : `sudo apt-get install tesseract-ocr tesseract-ocr-eng`
  * Fedora : `sudo dnf install tessearct`
  * Arch Linux: `sudo pacman -S tesseract tesseract-data-eng`
  

* Run `python setup.py install` to install requirements. Install script is still a work in progress.
* `[ ! -f ~/.fakemenot.config ] && cp fakemenot/twitter.config ~/.fakemenot.config`
* Go to https://apps.twitter.com/app/new and put your consumer and API keys in `~/.fakemenot.config`
* Run `fakemenot` after installation. Setup will install it in your path.

### Limitations
* Since it does OCR on the image, detection rate will vary on the quality of the screenshot.
* Only support desktop screenshots now. Universal support coming soon! :)

 
### Arguments

* `--image/-i`

Path to the screenshot image of tweet. Only works on Desktop screenshots.

* `--limit/-l`

Specify the number of tweets to pull from the detected user. Defaults to 100. Retweets are not pulled and does not affect the limit.


* `--config/-c`

Specify an alternate configuration file containing your twitter identification and authentication material.  Defaults to ~/.fakemenot.config

### Image Samples 

Tweet by @mattdm: 

![](http://i.imgur.com/5oDeoxv.png)

Output:

![](http://i.imgur.com/05ZeCxL.png)

**Blurry image**

Tweet by @elahmo: 

![](https://i.imgur.com/QI6ZOrA.png)

Output:

![](https://i.imgur.com/FY5jTJT.png)

**Fake image**

Tweet by @elahmo: 

![](https://i.imgur.com/zoDkJnf.png)

Output:

![](https://i.imgur.com/rd85pia.png)

