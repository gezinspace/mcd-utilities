# Running MCDGenerator #

Finally, once everything has been installed and the config file has been written you're ready to make some cards!  The quickest way is to provide the text to be MCD-ified on the command line.  For example

```
MCDGenerator --config mcdgenerator.conf  --output-file=mcds0428.txt 'その映画に興奮した。'
```

Here `config` is the config file from the previous set, `output-file` is the file in which to store your MCDs, and the text follows.  The output file name can be anything, I like to include the date.

When you run the command `MCDGenerator` will try to look up each word it encounters in order to put the definition on the back.  After running the first thing it will ask is

```
Looking up 映画
 映画 [えいが] /(n,adj-no) movie/film/(P)/
映画スター [えいがスター] /(n) film star/
映画ファン [えいがファン] /(n) cinema fan/cinema-goer/cinephile/film aficionado/film buff/film fan/movie buff/movie fan/
映画音楽 [えいがおんがく] /(n) film music/
映画化 [えいがか] /(n,vs) making (book) into film/making screen version/
映画会 [えいがかい] /(n) film society/movie club/

Definition? 
```

Respond with the definition you want to include.  If it's in the list `MCDGenerator` provided you can just cut-and-paste it.

After a few more of these `MCDGenerator` will exit.  You should then look over the file to make sure it's correct.  Mecab, kakasi, and the text-to-speech programs are pretty amazing, but they don't get everything right!

Once you're satisfied, start Anki.  Then go the "File" menu and choose "Import" (see [The Anki manual](http://ankisrs.net/docs/FileImport.html) for more on importing files).  You should get a screen that looks like this

<img src='http://mcd-utilities.googlecode.com/files/import.png'>

Click "Import".  Anki will report on how many cards were entered.  You can then go ahead and review them, just as with any other cards!<br>
<br>
After a while (I wait a week) You may want to remove the keywords.  You can do this with the <code>stripKeywords</code> program:<br>
<br>
<pre><code>stripKeywords --output-file mcds0428_stripped.txt --input-file mcds0428.txt<br>
</code></pre>

This will create a new file with all the definitions and sounds intact but with the keywords replaced by the standard <code>...</code>.  You can then import this into Anki in the same way and, if you want, delete or disable the old cards