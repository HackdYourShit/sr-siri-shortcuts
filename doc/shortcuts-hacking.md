# Shortcuts hacking

## Open API from Sveriges Radio

https://sverigesradio.se/oppetapi

### Live Broadcast Streams

https://sverigesradio.se/sida/gruppsida.aspx?programid=3756&grupp=10632

## Custom URL Scheme for Sveriges Radio Play

By poking around a little, I found out that the Play app from Sveriges Radio
supports a custom URL scheme. It works by passing the identifier for an episode
or channel like this:

`sesrplay://play/channel/203`
`sesrplay://play/episode/203`

## Importing Shortcuts by URL

https://www.reddit.com/r/shortcuts/comments/9t3214/icloud_shortcut_to_base64/
https://support.apple.com/guide/shortcuts/import-a-shortcut-from-a-url-apd77a47304b/ios

`data:text/shortcut;base64,ABC...`

## Converting Shortcut to Readable XML

Shortcuts are property list files in binary form by default. It is easy to
convert between binary and XML like this:

```sh
$ plutil -convert xml1 Example.shortcut
$ plutil -convert binary1 Example.shortcut
```
