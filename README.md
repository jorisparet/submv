# submv

[![pypi](https://img.shields.io/pypi/v/submv.svg)](https://pypi.python.org/pypi/submv/)
![version](https://img.shields.io/badge/python-3.6+-blue.svg)
[![license](https://img.shields.io/pypi/l/submv.svg)](https://en.wikipedia.org/wiki/GNU_General_Public_License)

**submv** allows you to shift a subtitle file by a given amount to synchronize it to a video stream using a simple command line tool.

Quickstart
----------

In a console, simply type

```bash
submv path/to/subtitles.srt -1.5
```

to shift the file `subtitles.srt` by -1.5s. By default, it will **overwrite** the original file.

More options:
- The shifted subtitles can be written to a new file by using the `--output` flag (or `-o` for short). Example: `submv file.srt 2.1 --output new_file.srt`.
- The default format is [SubRip](https://en.wikipedia.org/wiki/SubRip) (`*.srt` files). Other formats can be read using the `--format` flag (or `-f` for short). Example: `submv file.sub --format sub`.
- For certain formats such as [MicroDVD](https://en.wikipedia.org/wiki/MicroDVD) (`*.sub` files), the timecodes depend on the video framerate. To account for this, the correct framerate must be specified with the `--framerate` flag (or `-r` for short). Example: `submv file.sub --framerate 30`.

Installation
------------

**1.** From [PyPI](https://pypi.org/project/submv/):

```bash
pip install submv
```

----------

**2.** From the [code repository](https://github.com/jorisparet/submv):

```
git clone https://github.com/jorisparet/submv
cd submv
pip install .
```

#### Linux

The default folder should be under `/home/<user>/.local/bin/`. Make sure this location (or the correct one, if different) is included in your `$PATH` environment variable to be able to run the scripts from the console. If not, type the following command `export PATH=$PATH:/path/to/submv/script/` in the console or add it your `.bashrc` file.

#### Windows

The default folder should be under `C:\Users\<user>\AppData\Local\Programs\Python\<python_version>\Scripts\`. Make sure this location (or the correct one, if different) is included in your `$PATH` environment variable to be able to run the scripts from the console. If not, type the following command `set PATH=%PATH%;C:\path\to\submv\script\` in the console, or select `Edit the system environment variables` in the search bar, click `Environment Variables…`, click `PATH`, click `Edit...` and add the correct path to the scripts.

Author
------

[Joris Paret](https://www.jorisparet.com/)
