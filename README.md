# CMD-dactyl-manuform

This is a fork of [/carbonfet/dactyl-manuform](https://github.com/carbonfet/dactyl-manuform) which is a fork of the [Dactyl-ManuForm](https://github.com/tshort/dactyl-keyboard). The Dactyl-Manuform is a fork of the [Dactyl](https://github.com/adereth/dactyl-keyboard) with the thumb cluster from [ManuForm](https://github.com/jeffgran/ManuForm). Some features from the Dactyl Manuform Mini are kept along with new features added. 

I modified /src/dactyl_keyboard/dactyl.clj to produce a slightly modified thumb cluster and to produce fewer .scad files. These .scad files didn't 
play too well with my slicer, which is likely a result of my lack of knowledge in terms of clojure. I used Prusaslicer to remove the bottom 1mm of the 
left and right models. These are in the /stl directory. I also modelled a different controller board holder to accomodate the specific parts that I 
was able to obtain, which is also stored in the .stl directory. 

I plan to create a YouTube Video documenting the build and will post it when I have finished. 

## Features

- The use of sidenubs can be disabled. Sidenub should be disabled if you use Kailh, and Outemu. If you use Cherry MX, Gateron or Zealios switches, you can enable the sidenubs.
- Toggle for outer column between using 1.5u sized keys and 1u sized keys.
- If enabled, the rows which use 1.5u sized keys can be specified.
- Toggle for an extra row of keys for the outer column(s).
- Toggle for an extra inner column before the thumbcluster with (nrows-2) rows.
- Toggle between using the default thumb cluster, the mini thumb cluster designed by [l4u](https://github.com/l4u/dactyl-manuform-mini-keyboard), and a new thumb cluster.
- This new thumb cluster uses the same keycaps as the default, but is more compact. The thumb only has to move one position left or right from its neutral position to reach all the keys. 
- Removable controller board / TRRS jack holder as a separate part. This holder is then friction fit into a cutout on the back wall of the case. Designed for common TRRS breakout boards. 
- Models for both pro-micro and elite-c holders in the [things/](things/) directory. 

## Generate OpenSCAD and STL models

* Run `lein generate` or `lein auto generate`
* This will regenerate the `things/*.scad` files
* Use OpenSCAD to open a `.scad` file.
* Make changes to design, repeat `load-file`, OpenSCAD will watch for changes and rerender.
* When done, use OpenSCAD to export STL files



## License

Copyright © 2015-2018 Matthew Adereth, Tom Short and Leo Lou

The source code for generating the models is distributed under the [GNU AFFERO GENERAL PUBLIC LICENSE Version 3](LICENSE).

The generated models are distributed under the [Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0)](LICENSE-models).
