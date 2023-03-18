# amidon
A Mastodon client for Amiga computers

![Amidon logo](https://raw.githubusercontent.com/BlitterStudio/amidon/main/assets/Amidon_logo.png?token=GHSAT0AAAAAABYC2BDJD6TPVTE2SQ46QF6KZAVQTQQ)

<a rel="me" href="https://mastodon.social/@midwan">Follow me Mastodon!</a>

Amidon is a Mastodon native client for computers (or emulators) running AmigaOS 3.x.
It allows the user to connect and authenticate with a Mastodon server instance, post new toots and interact with the various aspects of Mastodon (replies, favourites, bookmarks, etc.).

## Requirements
- AmigaOS 3.x
- MUI 3.9 or newer (but see known issues for newer versions)
- 68020+ CPU
- 8MB of RAM
- An internet connection
- A web browser will be needed once, for the first time you authenticate your account

## Installation
Amidon is designed to be a portable application. Just place the binary in any directory you want and run it from there.  It will generate it's own settings and `cache` directory on startup.

### Known issues
- HTMLview, the MUI class used to display HTML content in Amidon, has issues with some versions of MUI on AmigaOS 3.x. It will not show any content on MUI 4 or 5, so it only works properly on MUI 3.9 currently. If you don't care about that functionality, you can of course use MUI 4 or 5 normally otherwise.
- HTMLview seems to have issues showing any content behind HTTPS links (e.g. images).
- MUI 3.8 also works, but it has several rendering issues with the content in the listviews, so it's not recommended.
- The HTML stripping functionality is not perfect, and sometimes strips away more than it should. Double clicking on an item will open it up in a separate window, containing the full HTML content (non-stripped), so you can use that as a workaround.
