# amidon
A Mastodon client for Amiga computers

![Amidon logo](https://raw.githubusercontent.com/BlitterStudio/amidon/main/assets/Amidon_logo.png)

<a rel="me" href="https://mastodon.social/@midwan">Follow me Mastodon!</a>

Amidon is a Mastodon native client for computers (or emulators) running AmigaOS 3.x.
It allows the user to connect and authenticate with a Mastodon server instance, post new toots and interact with the various aspects of Mastodon (replies, favourites, bookmarks, etc.).

![Amidon GUI](https://raw.githubusercontent.com/BlitterStudio/amidon/main/screenshots/Amidon_Publish.png)

## Requirements
- AmigaOS 3.x
- AmiSSL 4
- MUI 3.9 or newer (but see known issues for newer versions)
- The following MUI classes: 
  - `Hyperlink.mcc` (available in the MUI 4.x and 5.x archives)
  - [`TextEditor.mcc`](http://aminet.net/package/dev/mui/MCC_TextEditor-15.56)
  - [`BetterString.mcc`](http://aminet.net/package/dev/mui/MCC_BetterString-11.36) (required by TextEditor)
  - [`HTMLview.mcc`](http://aminet.net/package/dev/mui/MCC_HTMLview-13.4)
- [`codesets.library`](http://aminet.net/package/util/libs/codesets-6.21)
- 68020+ CPU
- 8MB of RAM
- An internet connection and a TCP/IP stack running (cURL will check for `bsdsocket.library` on startup). AmiTCP 4, Roadshow or emulators with the `bsdsocket.library` option enabled will work.
- A web browser will be needed once, for the first time you authenticate your account

## Installation
Amidon is designed to be a portable application. Just place the binary in any directory you want and run it from there.  It will generate it's own settings and `cache` directory on startup.

### Known issues
- It's slow to start-up on a real Amiga. I counted about 13 seconds on an 060/50 MHz from the moment you double-click on the icon. However, it's rather usable afterwards, so please be patient!
- HTMLview, the MUI class used to display HTML content in Amidon, has issues with some versions of MUI on AmigaOS 3.x. It will not show any content on MUI 4 or 5, so it only works properly on MUI 3.9 currently. If you don't care about that functionality, you can of course use MUI 4 or 5 normally otherwise.
- HTMLview seems to have issues showing any content behind HTTPS links (e.g. images).
- MUI 3.8 also works, but it has several rendering issues with the content in the listviews, so it's not recommended.
