### mutagen
---
https://github.com/quodlibet/mutagen

https://mutagen.readthedocs.io/en/latest/user/filelike.html

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

class IOInterface(object):
  
  def tell(self):
    raise NotImplementedError
    
  def read(self, size=-1):
    raise NotImplementedError
    
  def seek(self, offset, whence=0):
    raise NotImplementedError
    
  @property
  def name(self):
    raise NotImplementedError
    
  def write(self, data):
    raise NotImplementedError
    
  def truncate(self, size=None):
    raise NotImplementedError
    
  def flush(self):
    raise NotImplementedError
    
  def fileno(self):
    raise NotImplementedError
    
import mutagen
importgiofile
from gi.repository import Gio

gio_file = Gio.File.new_for_uri("
  http://people.xiph.org/~giles/2012/opus/ehren-paper_lights-96.opus")
cancellable = Gio.Cancellable.new()
with giofile.open(gio_file, "rb", cancellable=cancellable) as gfile:
  print(mutagen.File(gFile).pprint)


```

```
```

```
```


