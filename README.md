# XKCDAltTextBot

This Twitter bot replies to tweets from [@xkcdComic](https://twitter.com/xkcdComic) with the alt text of the most recent XKCD comic.

## Example

![Example of tweet from @xkcdComic and the reply from @XKCDAltTextBot](https://i.imgur.com/11PR1gm.png)

## Building and Running the Bot

This bot is designed to run on [Heroku](https://www.heroku.com/), but it should work on other cloud platforms, and can even run on your computer.

### General Instructions (Start here.)

Download the latest version of the bot as a ```.zip``` file [here], and extract it to your preferred folder.

Obtain your Twitter API and access keys [here](https://developer.twitter.com). Then, change the respective names of the environmental variables on lines 137-140 of [the program](xkcd_alt.py) in this format:

```python
key = [os.environ.get('YOUR_API_KEY_HERE_ALL CAPS', None),
           os.environ.get('YOUR_API_SECRET_KEY_HERE_ALL_CAPS', None),
           os.environ.get('YOUR_ACCESS_TOKEN_HERE_ALL_CAPS', None),
           os.environ.get('YOUR_ACCESS_SECRET_TOKEN_HERE_ALL_CAPS', None)]
```

Make all other modifications to the accounts you would like to interact with, and the formatting of your tweets. ([The official Twitter documentation is quite helpful for formatting.](https://developer.twitter.com/en/docs))

### --> Running on a PC

*This bot requires access to your environmental variables. The computer also needs to have [Python](https://www.python.org/) installed. Modify these steps as needed for macOS and Linux.*

You will need the [Requests](http://www.python-requests.org/en/latest/), [Requests-OAuthlib](https://requests-oauthlib.readthedocs.io/en/latest/), and [BeautifulSoup](https://www.crummy.com/software/BeautifulSoup/) libraries. If you have [Pipenv](https://pipenv.readthedocs.io/en/latest/), you can install them by running the command ```pipenv install``` inside the folder; otherwise, run ```pip install -r requirements.txt```.

Add your API keys and access tokens to your environmental variables by following [these instructions](https://java.com/en/download/help/path.xml). Then, just run ```python xkcd_alt.py``` in your command line and let it run! The bot respects the Twitter API limits, and will run every 60 seconds as long as the command line is open.

### --> Running on Heroku

Details are coming soon!

## Forks and Contributing

Feel free to fork this project and modify it for your own Twitter bot. (The license can be found [here](LICENSE).)

If you want to contribute to the project, open a pull request with your branch. If your changes modify the core function of the bot, you will need to ensure that it continues to work as expected, and gracefully handles failures.
