# slacTree
### SVG Large Annotated Circular Tree drawing program

A simple, extensible, Perl script for producing figures of large phylogenetic trees.

* While there are many other tree drawing programs, slacTree was originally written in 2009 to fill a need for producing publication quality figures of circular trees with more than 1000 taxa with custom annotations
* Because it is a single Perl script with very few dependencies, it is easy to run, and easy to further customize
* SVG is used because it is a scalable format allowing for very small representations of entire trees or highly magnified regions with unlimited resolution
* Circular and radial trees are more compact than linear representations

Examples
-----------

See [examples/](./examples) for a tutorial

*Abundance values from 3 datasets*

![ex5_combined](https://cloud.githubusercontent.com/assets/14023091/10204444/9f0c48c0-6770-11e5-9226-cf14c900981d.png)

*Magnified region; SVG allows for unlimited scaling*

![ex4 magnify](https://cloud.githubusercontent.com/assets/14023091/10204450/a66acdc6-6770-11e5-85bf-2db75fdcc300.png)

*Density plots of 3 datasets*

![ex5_density](https://cloud.githubusercontent.com/assets/14023091/10204448/a3b4b024-6770-11e5-920a-958dd07c6130.png)

Usage
-----

| File | Description |
|------|-------------|
| slacTree.pl | Main program for drawing SVG trees |
|  |  |
| config.txt | Default settings |
| default_annotations.txt | Annotations and comments added to new slacTree files |
| make_density_jpg.r | Run by slacTree.pl to create density background JPGs |
| convert_old_treeinfo.pl | Converts older versions of slacTree or treeinfo files |
| [examples/](./examples/) | Tutorial examples |

```
Usage: slacTree.pl [command] (options)

commands:
newick2st     newick file -> basic slactree
st2newick     slactree file -> newick
tree          slactree file -> SVG
density       slactree file -> density plot overlay SVG
zlim          calculate scaling factor (for multiple plots)

options:
-d            output density/abundance base file
-f            force overwrite of output file (default: no overwrite)
-h            show help
-i file       input file (use '-' for STDIN)
-o file       output file (default: STDOUT)
-t file       taxonomic data file (optional)
-z num        scaling factor (for multiple plots)
```

Dependencies
------------

* Perl (https://www.perl.org/get.html)
* R (https://cran.r-project.org/)
