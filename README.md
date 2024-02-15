# Top last.fm artists seen live

[![Run](https://github.com/matsest/lastfm-artists-seen-live/actions/workflows/run.yaml/badge.svg?event=schedule)](https://github.com/matsest/lastfm-artists-seen-live/actions/workflows/run.yaml)

> Which of my top last.fm (most listened to) artists have I seen or not seen live?

## Background

To answer the question above I'm using scrobbles from [my last.fm account](https://www.last.fm/user/matsest), the ['seen live' tag](https://www.last.fm/tag/seen+live) on my last.fm artists and the [last.fm API](https://www.last.fm/api) together with some PowerShell.

## Usage

### Prerequisites

  - [PowerShell 7.x](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell)
  - [Last.FM API Account](https://www.last.fm/api/account/create)

### Run script

```powershell
$env:API_KEY = "<API Key>"
./src/main.ps1 [[-LastFmUserName] <string>] `
         [[-NumberOfArtists] <string>] `
         [[-InactiveArtistsFile] <string>] `
         | Out-File artists.md
```

### Result

An up-to-date version of my list of artists (generated by GitHub Actions each night) can be found in the [artists.md](artists.md) file.

See the latest run in [Actions](https://github.com/matsest/lastfm-artists-seen-live/actions).

## License

[MIT License](./LICENSE)
