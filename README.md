# .obj-file-detection
.obj file load and display , along with .mtl file
<https://github.com/animeshsrivastava24>
<animeshsri.nith@gmail.com>
The .obj file is an extension of 3d image I have created a method how to load and display such files.

Src Credit : https://www.pygame.org/wiki/OBJFileLoader This code provides a function for loading a model from a wavefront OBJ file (3d model format) into an OpenGL display list. It additionally loads any referenced material and texture files. It does not support multiple models in the OBJ file, nor any material properties other than diffuse colour (Kd) and diffuse texture (map_Kd).

1.We used the objloader.py and main.py
2.To load and display .obj file we download it from the net
3.Generally .obj file will not have any reference to .mtl inside its code
4.Some knowledge

Wavefront .obj file
OBJ (or .OBJ) is a geometry definition file format first developed by Wavefront Technologies for its Advanced Visualizer animation package. The file format is open and has been adopted by other 3D graphics application vendors.
Material template library
MTL material format Filename extension 	.mtl
Developed by 	Wavefront Technologies
Type of format 	3D texture format
Synopsis

In 3D Computer Graphics, one of the most common geometry interchange file formats is the OBJ. The .MTL File Format is a companion file format that describes surface shading (material) properties of objects within one or more .OBJ files. A .OBJ file references one or more .MTL files (called "material libraries"), and from there, references one or more material descriptions by name.
Introduction

The Material Template Library format (MTL) is a standard defined by Wavefront Technologies for ASCII files that define the light reflecting properties of a surface for the purposes of computer rendering, and according to the Phong reflection model. The standard has widespread support among different computer software packages, making it a useful format for interchange of materials.

MTL files are commonly accompanied by and referenced from OBJ files that define geometry upon which the materials of the MTL file are mapped.

The MTL format, although still widely used, is outdated and does not fully support later technologies such as specular maps and parallax maps. However, due to the open and intuitive nature of the format, these can easily be added with a custom MTL file generator.

The MTL format defines a number of formats.
MTL file is used to give color and texture to .obj file- every .obj file has its .mtl file,it can be created using reference from internet.
5.The object file we loaded from the internet has the cube.obj and cube.mtl file , and thus cube.obj has reference to cube.mtl in it, if the cube.obj doesn't have reference to cube.mtl we dont need cube.mtl and we only get outline/wavefront.
Src to load file :https://gist.github.com/noonat/1131091
But in the above objloader.py we have function defined for mtl 
so we need mtl file also here to run.
I will be posting how to load and display .obj file without .mtl file.
Alternative: If you want to display any .obj file and you don't have the .mtl file with it,no worry use the cube.mtl file because it is only used to give texture and color so we can associate it with any .obj file.How to proceed download the .obj file and see cibe.obj file and use the commands from cube.obj and add mtl file codes to our .obj file ,now we are ready to go
rename the .mtl file with name of obj file loaded and run it.
:) Happy Reading
