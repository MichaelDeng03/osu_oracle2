# 🔮 osu!Oracle

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install required dependencies.

```bash
pip install -r requirements.txt
```

Until oAuth authentication with osu! is implemented, API credentials are stored in a file named `osu_access_token.py`, which must be created in either the base folder `/` with system path inserting `sys.path.insert(0, "../")` in each module that requires api access, or in `data/` and `scraping/`. API credentials may be generated in your osu! settings under OAuth.

An example file looks like the following:

```python
client_id = 13337
client_secret = "supersecretrandomstringfromosu"
```

## File structure

```bash
# Web application and user-input handling.
osu_oracle/

# Model training and saved models.
Models/

# Used to store osu! data w/ a notebook for creating the sqlite db schema. Also contains classes for mediating interactions between ossapi and the database.
data/

# Handy scripts to scrape osu! & store data.
scraping/
```

## Try it out

osu!Oracle is currently hosted live at osu-oracle.com.

## Contributing?

Database schema can be found here: <https://dbdiagram.io/d/osu-654e8e887d8bbd6465f40357>.

Please open an issue on github for a copy of the database, or scrape it yourself using the scripts provided in `/scraping.` `scrape_user_ids.py` will pull all ids from osu! leaderboards, `scrape_users.py` will pull all user data and top scores from those ids, and `scrape_maps.py` will pull all map data from the users' top 100 plays. Expect these scripts to run for about ~35hours in total due to osu! API rate limits.

## Disclaimer

This project is not associated or endorsed by osu.ppy.sh and peppy. If you have any questions or concerns please reach out to me on this repository.
