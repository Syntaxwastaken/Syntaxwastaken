```python

from dataclasses import dataclass
from typing import Tuple


class Meta(type):
    def __new__(cls, name, bases, attrs):
        new_cls = super().__new__(cls, name, bases, attrs)
        return dataclass(unsafe_hash=True, frozen=True)(new_cls)


class Bio(metaclass=Meta):
    name        : str = "SyntaX ErroR"
    im          : str = "Website Dev, Minecraft Dev, Programmer"


class Stack(metaclass=Meta):
    languages   : Tuple[str, ...] = ("HTML", "CSS", "JS", "C++", "Python", "React")
    databases   : Tuple[str, ...] = ("MySQL", "Mongo", "Redis")
    ongoing     : Tuple[str, ...] = ("TS", "Go")


class Social(metaclass=Meta):
    discord     : str = "sYɴᴛᴀ᙭ ΣʀʀᴏR#5679"
    twitter     : str = "syntax_OP"
    twitch      : str = "theinfinitypro"
    replit      : str = "syntaxnotfound"


class Misc(metaclass=Meta):
    MT website  : str = "https://minetown.games"
    MT discord  : str = "https://join.minetown.games"
```
