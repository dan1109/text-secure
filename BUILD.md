
## Dependencies

[ActionBarSherlock >=4.2.0](https://api.github.com/repos/JakeWharton/ActionBarSherlock/tarball/4.2.0)

To get the dependencies and update ```project.properties``` on the commandline,
do:

```
$ cd libs && wget -o sherlock.tar.gz https://api.github.com/repos/JakeWharton/ActionBarSherlock/tarball/4.2.0 && tar xvzf sherlock.tar.gz
$ mv libs/android-support-v4.jar libs/JakeWharton-ActionBarSherlock*/library/libs/android-support-v4.jar
$ android update lib-project -p libs/JakeWharton-ActionBarSherlock*/library -t android-17
$ android update project --target android-17 --path . --name text-secure -s
```

After that, Apache ant can be used to compile TextSecure without using Eclipse.

```
$ ant clean && ant debug
```

## Application level debugging

To enable, place ```android:debuggable="true"``` in the ```<application>```
attribute of the ```build.xml``` file.
