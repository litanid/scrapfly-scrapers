# Threads.net Scraper

This scraper is using [scrapfly.io](https://scrapfly.io/) and Python to scrape Threads.net post and profile data.

Full tutorial <https://scrapfly.io/blog/how-to-scrape-threads/>

The scraping code is located in the `threads.py` file. It's fully documented and simplified for educational purposes and the example scraper run code can be found in `run.py` file.

This scraper scrapes:
- Threads.net Thread (aka post) data
- Threads.net Profile data

For output examples see the `./results` directory.

Note: This scraper is only scraping public Threads data that doesn't require a login to access.

## Setup and Use

This Threads.net scraper is using Python with [scrapfly-sdk](https://pypi.org/project/scrapfly-sdk/) package which is used to scrape and parse Threads' data.

1. Retrieve your Scrapfly API key from <https://scrapfly.io/dashboard> and set `SCRAPFLY_KEY` environment variable:
    ```shell
    $ export SCRAPFLY_KEY="YOUR SCRAPFLY KEY"
    ```
2. Clone and install Python environment:
    ```shell
    $ git clone git@github.com:scrapfly/scrapfly-scrapers.git
    $ cd scrapfly-scrapers/threads-scraper
    $ poetry install .
    ```
3. Run example scrape:
    ```shell
    $ poetry run python run.py
    ```
4. Run tests:
    ```shell
    $ poetry install --with dev
    $ poetry run pytest test.py
    # or specific scraping areas
    $ poetry run pytest test.py -k test_thread_scraping
    $ poetry run pytest test.py -k test_user_scraping
    ```

