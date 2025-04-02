# Setup Dictionary in Linux

02-04-25

I followed arch linux [wiki](https://wiki.archlinux.org/title/Dictd).

First install `dictd`.

```
$ sudo pacman -S dictd
```

I want to use it offline.
Disable online mode by going to `/etc/dict/dict.conf` and comment line `server dict.org`.

```
server localhost
# server dict.org
```

Then install WordNet and Moby Thesaurus.

```
$ yay -S dict-wn
$ yay -S dict-moby-thesaurus
```

Enable and start the service.

```
$ systemctl enable dictd.service
$ systemctl start dictd.service
```

Now to list installed dictionaries:

```
$ dict -I
  dictd 1.13.3/rf on Linux 6.11.9-arch1-1
  On magic: up 93.000, 3 forks (116.1/hour)

  Database      Headwords         Index          Data  Uncompressed
  wn                 147483       3005 kB       9278 kB         29 MB
  moby-thesaurus      30263        528 kB         28 MB         28 MB
```

To query the dictionary just enter a word:

```
$ dict word
```
