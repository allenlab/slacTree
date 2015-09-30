# slacTree
### SVG Large Annotated Circular Tree drawing program

A simple, extensible, Perl script for producing figures of large phylogenetic trees.

* While there are many other tree drawing programs, slacTree was originally written in 2009 to fill a need for producing publication quality figures of circular trees with more than 1000 taxa with custom annotations
* Because it is a single Perl script with very few dependencies, it is easy to run, and easy to further customize
* SVG is used because it is a scalable format allowing for very small representations of entire trees or highly magnified regions with unlimited resolution
* Circular and radial trees are more compact than linear representations

![slacTree multi-dataset figure](docs/screenshot_combined.png multi-dataset abundance figure)

![magnified](docs/screenshot_magnify.png magnified region)

![density plots](docs/screenshot_density.png density plots)


| File | Description |
|------|-------------|
| slacTree.pl | Main program for drawing SVG trees |
|  |  |
| config.txt | Default settings |
| default_annotations.txt | Annotations and comments added to new slacTree files |
| make_density_jpg.r | Run by slacTree.pl to create density background JPGs |
| convert_old_treeinfo.pl | Converts older versions of slacTree or treeinfo files |
| [examples/](./examples/) | Tutorial examples |

Usage
-----

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
-f            force overwrite of ouput file (default: no overwrite)
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
