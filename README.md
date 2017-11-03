yarpviz
=======

The `yarpviz` is a graphical tool for profiling and visualizing Yarp network! 

![scenario2](/src/resources/yarpviz.png)

:warning: :warning: `yarpviz` has been integrated in [YARP](https://github.com/robotology/yarp/tree/devel) (release 2.3.72).

Dependencies
------------
 - Qt5
 - GraphViz library 
 
### Linux 

`sudo apt-get install libgraphviz-dev`

### Windows

download and install the library from (http://www.graphviz.org/Download_windows.php).

Set `GRAPHVIZ_ROOT` to point the installed directory (usually `C:\Program Files\Graphviz2.38` or `C:\Program Files (x86)\Graphviz2.38`).

Append `%GRAPHVIZ_ROOT%\bin` to your PATH variable.


Installation
------------

```
$ cd yarpviz
$ mkdir build; cd build;
$ cmake ../; make 
```



