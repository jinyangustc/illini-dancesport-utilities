# Illini Dancesport Utilities

## Sync Event Service Space Request Confirmation with Google Calendar

[cal.py](cal.py)

Please refer to [Google Calendar Python
Quickstart](https://developers.google.com/calendar/api/quickstart/python) for
Authorization setup.

## Google Contact Sync

[contacts.py](contacts.py)

## Generate Rounds File

### Preparation

Unzip announcement `mp3`s:

```bash
unzip playlists/announcements.zip -d playlists/
```

Generate a 30s silence `mp3`:

```bash
python rounds.py silence --duration=30
mv silence.mp3 playlists/
```

### Define playlists and generate rounds files

Define your playlist in a `.ini` file. See files in [playlists](playlists) for examples.

Then run `python3 rounds.py run <your_playlist>.ini` to download, trim and concatenate songs into one round file.

For example, running

```bash
python3 rounds.py run playlists/standard_1.ini
```

will produce a standard rounds file `standard_1.mp3` in `playlists/`.
