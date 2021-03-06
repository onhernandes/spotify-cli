# spoticly

Tiny CLI for play/pause/next/prev on Spotify :sparkles:

# Install

```sh
$ pip install git+https://github.com/onhernandes/spoticly.git --user
```

# Usage

First, create an application on [Spotify's Dev Dashboard](https://developer.spotify.com/dashboard/login) for getting a client ID, client secret. Remember to specify your application as non-commercial. Then edit your application and create a redirect URI, you can use `http://localhost/spoticly/callback`. You don't actually need a server running, you will just need the URL with `?code=` at the end.

Run `spoticly config`, then set your username, client ID, client secret and redirect URI. You can run the same command if you wanna change something.

After settings your config properly, run `spoticly auth`. This will open your webbrowser for signing in with your's Spotify account. You will be redirected to the URL you set before, after being redirected, just copy the whole URL - including the `?code=` part, that's important - and paste on your terminal. Spotify will be authenticated and you will see something like `User <name> authenticated!`. This will save your current access token and also your refresh token, so you won't need to re-authenticate for a while.

After authenticated, you can now control your playback from the terminal!

Run `spoticly --help` for more.

All playback commands are related to current playing device.

## Examples

- `spoticly auth` - authenticates your user
- `spoticly config` - sets your config(like, Client ID, Client Secret, Username, etc)
- `spoticly next` - plays next track on current playing device
- `spoticly prev` - plays previous track on current playing device
- `spoticly pause` - pauses current playing device
- `spoticly resume` - resume previously paused track on current playing device

# Questions and more

If you've ideas, issues or anything else, just open an issue!
