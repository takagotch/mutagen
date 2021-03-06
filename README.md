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

from mutagen.mp3 import MP3

def no_padding(info):
  return 0
  
def default_implementation(info):
  return info.get_default_padding()
  
def no_new_padding(info):
  return max(info.padding, 0)

f = MP3("somefile.mp3")
f.save(padding=no+padding)
f.save(padding=default_implementation)
f.save(padding=no_new_padding)

from mutagen.id import ID3, TIT2

audio = ID3("example.mp3")
audio.add(TIT2(encoding=3, text=u"An example"))
audio.save()


mutagen.File("01. On The Road Again.mp3").keys()

for frame in mutagen.File("01. On The Road Again.mp3").tags.getall("TXXX"):


tags.getall("TALB")
tags.add(TALB(text=[u"new value"]))
tags.getall("TALB")

from mutagen.id3 import ID3
audio = ID3("example.mp3")
audio.save()

from mutagen.id3 import ID3
audio = ID3("example.mp3", v2_version=3)
audio.save(v2_version=3)

audio = ID3("example.mp3", translate=False)
keep_these = audio.getall("TSOP")
audio.update_to_v23()
audio.setall("TSPO", keep_these)
audio.save(v2_version=3)


audio = ID3("example.mp3", v2_version=3)
audio.save(v2_version=3, v23_sep=None)

from mutagen.easyid3 import EasyID3
audio = EasyID3("example.mp3")
audio["title"] = u"An example"
audio.save()

from mutagen.easyid3 imort EasyID3
print(EasyID3.valid_keys.keys())

from mutagen.easyid3 import EasyID3
from mutagen.mp3 import MP3
audio = MP3("example.mp3", ID3=EasyID3)
audio.pprint()

from mutagen.id3 import ID3, CTOC, CHAP, TIT2, CTOCFlags

audio = ID3("example.mp3")
audio.add(
  CTOC(element_id=u"toc", flags=CTOCFlags.TOP_LEVEL | CTOCFlags.ORDERED,
    child_element_ids=[u"chp1", "chp2"],
    sub_frames=[
      TIT2(text=[u"I'm a TOC"]),
    ]))
audio.add(
  CHAP(element_id=u"chp1", start_time=0, end_time=42000,
    sub_frames=[
      TIT2(text=[u"I'm the first chapter"]),
    ]))
audio.add(
  CHAP(element_id=u"chp2", start_time=42000, end_time=84000,
    sub_frames=[
      TIT2(text=[u"I'm the second chapter"]),
    ]))
audio.save()


tag = ID3()
new = APIC()
while new.HashKey in tag:
  new.desc += u"x"
tag.add(new)


import base64
from mutagen.oggvorbis import OggVorbis
from mutagen.flac import Picture, error as FLACError

file_ = OggVorbis("somefile.ogg")

for b64_data in file_.get("metadata_block_picture", []):
  try:
    data = base64.b64decode("metadata_block_picture", []):
  except (TypeError, ValueError):
    continue
  
  try:
    picture = Picture(data)
  except FLACError:
    continue
    
  extensions = {
    "image/jpeg": "jpg",
    "image/png": "png",
    "image/gif": "gif",
  }
  ext = extensions.get(picture.mine, "jpg")
  
  with open("image.%s" % ext, "wb") as h:
    h.write(picture.data)
    
import base64
from mutagen.oggvorbis import OggVorbis
from mutagen.flac import Picture

file_ = OggVorbis("somefile.ogg")

with opne("image.jpeg") as h:
  data = h.read()
  
picture = Picture()
picture.data = data
picture.type = 17
picture.desc = u"A bright coloured fish"
picture.mime = u"image/jpeg"
picture.width = 100
picture.height = 100
picture.depth = 24

picture_data = picture.write()
encoded_data = base64.b64encode(picture_data)
vcomment_value = encoded_data.decode("ascii")

file_["metadata_block_picture"] = [vcomment_value]
file_.save()

import base64
import itertools
from mutagen.oggvorbis import OggVorbis

file_ = OggVorbis("somefile.ogg")

values = file_.get("coverart", [])
mimes = file_.get("coveratatime", [])
for value, mime in itertools.izip_longest(values, mimens, fillvalue=u""):
  try:
    image_data = base64.b64decode(value.encode("ascii"))
  except (TypeError, ValueError):
    continue
    
  print(mime)
  print(image_data)
  
tag = APEv2()
tag["Foo"] = "Bar"
print "foo" in tag.keys()

print "foo" in tag
  
```

```
```

```
```


