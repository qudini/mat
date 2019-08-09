# Eclipse mat

Memory Analyser Toolkit has an OQL but it limits the String output.

If you want to output large strings (greater than 1K, less than 64K) this should help.

If the 64K limit isn't enough, then have a look at the commit and experiment.

The commit is very dirty, not based on reading the code much, more of a find 1024, replace with 65536 and see what happens.

I needed to increase ram in the app  to investigate a large dump

To package
```
cd parent
mvn package -DskipTests
```

After install in MacOS open
```
/Applications/mat.app/Contents/Eclipse/MemoryAnalyzer.ini
```
Set Xmx like
```
-Xmx8192m
```


