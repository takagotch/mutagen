### mutagen
---
https://github.com/quodlibet/mutagen

```py
from mutagen.oggvorbis import OggVorbis
f = OggVorbis("11. The way It Is.ogg")
type(f)


type(f.info)
print(f.info.pprint())

from mutagen.id3 import ID3
m = ID3("08. Firestarter.mp3")
type(m)


from mutaagen import MutagenError

try:
  f = OggVorbis("11. The way It Is.ogg")
except:
  print("Loading failed :(")







```

```
```

```
```


