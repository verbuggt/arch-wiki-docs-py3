# arch-wiki-docs-py3
A python3 only version of the arch-wiki-docs package with less python2. 

if you want to download the entire arch wiki for offline availability, so you can confidently wreck your network drivers and such but don't like python2, you can use this.

it's basically the same as the [original](https://archlinux.org/packages/community/any/arch-wiki-docs/) with the old py2 libraries replaced with their py3 counterparts and some required fixes

## installation
0. download and cd<br>
`git clone https://github.com/verbuggt/arch-wiki-docs-py3.git && cd arch-wiki-docs-py3`

1. create virtual python environment<br>
`python3 -m venv venv && source venv/bin/activate`

2. install requirements<br>
`pip3 install -r requirements.txt`

3. apply patches<br>
on linux/osx: `cp simplemediawiki.py venv/lib/python*/site-packages/`<br>
on windows: move the simplemediawiki.py to `venv/lib/python3.X/site-packages/`

4. run the thing (all languages - for specific language see below)<br>
`python3 arch-wiki-docs.py --output-directory wiki`

## language selection
to download the wiki in **English only** run:

```console
dingus@bingus:~$ python3 arch-wiki-docs.py --output-directory wiki --lang en
```

## issues
Language selection only works for English<br>
so this will not work:

```console
dingus@bingus:~$ python3 arch-wiki-docs.py --output-directory wiki --lang de
```

if you want any other language, you need to edit the file `Arch-Wiki/ArchWiki.py` and change `local_language` (line 16) to your desired language (locale name)

so for German, that would mean changing `local_language` to `"Deutsch"`

## TODO
maybe fix language selection<br>
priority: -2

---
ok thats it :3<br>
