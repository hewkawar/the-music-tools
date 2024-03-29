# The Music Tools
![GitHub Actions Workflow Status](https://img.shields.io/github/actions/workflow/status/hewkawar/the-music-tools/publish.yml)
[![npm version](https://badge.fury.io/js/the-music-tools.svg)](https://badge.fury.io/js/the-music-tools) 
![NPM Unpacked Size](https://img.shields.io/npm/unpacked-size/the-music-tools)
[![install size](https://packagephobia.com/badge?p=the-music-tools)](https://packagephobia.com/result?p=the-music-tools)
![NPM Downloads](https://img.shields.io/npm/dt/the-music-tools)

[![HitCount](https://hits.dwyl.com/hewkawar/the-music-tools.svg?style=flat)](http://hits.dwyl.com/hewkawar/the-music-tools) 
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/hewkawar/the-music-tools)
![GitHub Issues or Pull Requests](https://img.shields.io/github/issues-pr/hewkawar/the-music-tools)
![GitHub Release Date](https://img.shields.io/github/release-date/hewkawar/the-music-tools)

 ---
Music Downloader for npmjs

## Installing
### Package manager

Using npm:
```bash
$ npm i the-music-tools
```

Using yarn:
```bash
$ yarn add the-music-tools
```

Using pnpm:
```bash
$ pnpm add the-music-tools
```

Once the package is installed, you can import the library using `import` or `require` approach:

```js
import { Music } from 'the-music-tools';

const music = new Music();
```

You can also use the default export, since the named export is just a re-export from the Axios factory:
```js
import themusic from 'the-music-tools';

const music = new themusic.Music();
```

If you use `require` for importing, **only default export is available**:
```js
const themusic = require('the-music-tools');

const music = new themusic.Music();
```

## Example
> **Note**: CommonJS usage  
> In order to gain the TypeScript typings (for intellisense / autocomplete) while using CommonJS imports with `require()`, use the following approach:

```js
import { Music } from 'the-music-tools';
//const { Music } = require('the-music-tools'); // legacy way

const music = new Music();

const YoutubeSearch = music.searchYoutube('something');
// Search Video

const YoutubeVideo = music.getYoutubeVideo('dQw4w9WgXcQ');
// Get Video Detail

const YoutubeBuffer = music.downloadYoutubeVideo('dQw4w9WgXcQ');
// Get sound Buffer from 'dQw4w9WgXcQ'

music.downloadYoutubeVideoToFilename('dQw4w9WgXcQ', 'downloads/youtube-sound.mp3');
//  Download sound from 'dQw4w9WgXcQ' to file 'downloads/youtube-sound.mp3'

// if want to use sound from Spotify
music.spotifyLogin({
    clientId: 'YOUR_SPOTIFY_CLIENT_ID',
    clientSecret: 'YOUR_SPOTIFY_CLIENT_SECRET'
});

const SpotifySearch = music.searchSpotify('something');
// Search Track

const SpotifyTrack = music.getSpotifyTrack('1dGr1c8CrMLDpV6mPbImSI');
// Get Spotify Song Track

const SpotifyBuffer = music.downloadSpotifyTrack('1dGr1c8CrMLDpV6mPbImSI');
// Get sound Buffer from '1dGr1c8CrMLDpV6mPbImSI'

music.downloadSpotifyTrackToFilename('1dGr1c8CrMLDpV6mPbImSI', "downloads/spotify-track.mp3")
//  Download sound from '1dGr1c8CrMLDpV6mPbImSI' to file 'downloads/spotify-track.mp3'
```
