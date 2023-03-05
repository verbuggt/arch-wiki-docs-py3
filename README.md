# arch-wiki-docs-py3
A python3 only version of the arch-wiki-docs package with less python2. 

if you want to download the entire arch wiki for offline availability so you can confidently wreck your network drivers and such but don't like python2, you can use this.

it's basically the same as the [original](https://archlinux.org/packages/community/any/arch-wiki-docs/) with old py2 libraries replaced with their py3 counterparts and some required fixes

## usage
to download **all** languages run:

```console
dingus@bingus:~$ python3 arch-wiki-docs.py --output-directory wiki
```

## issues

Language selection is kinda broken.
so this will not work:

```console
dingus@bingus:~$ python3 arch-wiki-docs.py --output-directory wiki --lang de
```

if you only want the English version, putting `en` works tho.

if you want any other language, you need to edit the file `Arch-Wiki/ArchWiki.py` and change `local_language` (line 16) to your desired language (locale name)

so for German, that would mean changing `local_language` to `Deutsch`

## todo
maybe fix language selection<br>
priority: -2

---
ok thats it :3<br>
