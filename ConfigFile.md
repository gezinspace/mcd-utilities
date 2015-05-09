# Setting up the configuration file #

Once you've downloaded all the necessary pieces you need to set up a configuration file in order to tell `MCDGenerator` where to find them, plus a few other things.  The file can be named anything you like, but it must be created in a text editor like vi, Emacs, Notepad, gedit, etc rather than a word processor.  A sample configuration file looks like something like this:

```
mecab = /opt/local/bin/mecab
mecab_config = /opt/local/etc/mecabrc
kakasi = /opt/local/bin/kakasi
kakasi_itaijidict = /opt/local/etc/itaijidict
kakasi_kanwadict  = /opt/local/etc/kanwadict
keyword_file = /home/me/heisig-keywords
reader = kyoko
sound_dir = /home/me/Dropbox/Public/Anki/Japanese MCDs.media
```


Each line is a name and a value connected by '='.  Instructions for OS X and Linux are below.  Again, my apologies to people using Windows, but I don't know how to set things up there.  If anyone can offer assistance I'd appreciate it!

### mecab and kakasi ###

The location where you installed mecab and kakasi

  * On OS X, if you used the Japanese plugin, these would be
    * `/Users/(your login name)/Library/Application Support/Anki/plugins/japanese/osx/mecab/bin/mecab`
    * `/Users/(your login name)/Library/Application\ Support/Anki/plugins/japanese/osx/kakasi/kakasi`
  * On Linux you will not need these unless you installed these programs in a non-standard way.  If you `mecab --help` and {{kakasi --help}} on the command line both work, then you don't need to do anything else.

### mecab\_config ###

This is the location of mecab's config file.  It is probably the same as the value you used for `mecab`, just replace `bin/mecab` with `etc/mecabrc`.  Again, under Linux if you used a standard installation you probably won't need this.

### kakasi\_itaijidict and kakasi\_kanwadict ###

These are the locations of support files for Kakasi

  * On OS X, if you used the Japanese plugin, these would be
    * `kakasi_itaijidict = /Users/(your login name)Library/Application Support/Anki/plugins/japanese/osx/kakasi/itaijidict`
    * `kakasi_kanwadict  = /Users/(your login name)/Library/Application Support/Anki/plugins/japanese/osx/kakasi/kanwadict`
  * On Linux these will depend on how you installed these programs. For Debian-based systems (which I think includes Ubuntu), see the example below.

### keyword\_file ###

This is the file of Heisig keywords, available from [this project](http://mcd-utilities.googlecode.com/git/heisig_keywords).  Just download this keyword file and set the location in the config file.

### reader ###

If you want to use a Text-to-speech program to read your cards then include this line.  People using OS X "Lion" can set this to "Kyoko" to use the built-in Japanese voice.  Everyone else should set this to "google" to use Google's text-to-speech system.

### sound-dir ###

This is where the media files for your deck should be stored.  See the [Anki media instructions](http://ankisrs.net/docs/SyncingMedia.html) for details on setting this up.  If you do not want audio for you cards just leave out this line.


### OS X example ###

Here is the file I use under OS X.  You may just need to change "Larne" to your username and change the sound directory to match the name of your MCD deck.  If you are not using Lion you'll also need to change `reader` to `google`

```
mecab = /Users/Larne/Library/Application Support/Anki/plugins/japanese/osx/mecab/bin/mecab
mecab_config = /Users/Larne/Library/Application Support/Anki/plugins/japanese/osx/mecab/etc/mecabrc
kakasi = /Users/Larne/Library/Application Support/Anki/plugins/japanese/osx/kakasi/kakasi
keyword_file = /Users/Larne/mcd-utilities/heisig_keywords
kakasi_itaijidict = /Users/Larne/Library/Application Support/Anki/plugins/japanese/osx/kakasi/itaijidict
kakasi_kanwadict  = /Users/Larne/Library/Application Support/Anki/plugins/japanese/osx/kakasi/kanwadict
reader = kyoko
sound-dir = /Users/Larne/Dropbox/Public/Anki/Japanese MCDs.media
```


### Linux example ###

Here is the file I use under Linux (Debian Squeeze).  You might just need to change `larne` to your username and `sound_dir` to match the name of your deck

```
kakasi_itaijidict = /usr/share/kakasi/itaijidict
kakasi_kanwadict  = /usr/share/kakasi/kanwadict
keyword_file = /home/larne/mcd-utilities/heisig_keywords
reader = google
sound_dir = /home/larne/Dropbox/Public/Anki/Japanese MCDs.media
```