# Introduction #

mcd-utilies consists of two main programs
  * `MCDGenerator` reads chunks of Japanese text and creates a file of MCDs.  Clozed kanji is replaced by the Heisig keyword
  * `stripKeywords` removes the keywords from a previous batch of MCDs, replacing them with the standard three dots

The idea is to initially create MCDs with keywords replacing the kanji as an easy first step.  Then, after a week or so, remove the keywords for the full benefit of MCDs.

MCDGenerator is a command-line tool, not an application or Anki plugin.  I'm afraid it is not as user-friendly as I would like.  In addition, it requires a number of other programs to be installed and some configuration.  I hope the instructions here will be somewhat clear, please report any problems or difficulty you may run into.

## Installation ##

  * [Install on OSX](InstallOSX.md)
  * [Install on Linux](InstallLinux.md) (I've only tested on Debian Squeeze, but it should work on other distributions)
  * **Windows** Unfortunately I don't know anything about Windows and have no access to a Windows machine.  It should be possible to run on Windows, since it uses the same software that the Anki Japanese plugin uses.  Please check out the instructions for the other platforms and if you have any success please let me know!

## Configuration ##

Once all the pieces are installed you need to create a configuration file.

  * [Setting up the configuration file](ConfigFile.md)

## Running ##

Once you've got everything installed and the config file set up you can run `MCDGenerator` to make cards which you can import into anki.  Later, run `stripKeywords` to remove the keywords.

  * [Running MCDGenerator](RunMCDGenerator.md)
  * [Running stripKeywords](RunStripKeywords.md)