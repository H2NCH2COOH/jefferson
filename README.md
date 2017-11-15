# jefferson
JFFS2 filesystem extraction tool

Based on [sviehn's jefferson](https://github.com/sviehb/jefferson)

Removed multiple fs handling and handle duplicate inode number by its version

Installation
============
```bash
$ sudo python setup.py install
```


Dependencies
============
- `cstruct`
- `pyliblzma`

```bash
$ sudo pip install cstruct
$ sudo apt-get install python-lzma
```

Features
============
- Big/Little Endian support
- `JFFS2_COMPR_ZLIB`, `JFFS2_COMPR_RTIME`, and `JFFS2_COMPR_LZMA` compression support
- CRC checks - for now only enforced on `hdr_crc`
- Extraction of symlinks, directories, files, and device nodes

Usage
============
```bash
$ jefferson filesystem.img -d outdir
```
