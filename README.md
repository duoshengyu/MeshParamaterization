# MeshParamaterization
This is a mesh paramaterize program.
Refer to Mesh Parameterization Methods and Their Applications Chapter 3
by Alla Sheffer .al.2006

Platform:           Windows 10

Develop Tool:       Visual Studio 2013

Program language:   C++  OpenGL

External libraries: glfw glew OpenMesh eigen

usage:

1.Download zip or clone this repository.

2.Open "OpenGL.sln" using Visual Studio 2013(Only test in version 2013 now).

3.Change the Configuration to Release.

4.Run.
In this step you may see "something.dll are not in your compute" something like this,
go "lib" sub folder and copy the "something.dll" file to "Release" folder.After this,
it should work.

Process usage:

This process only supprt .off file now.

In Command Prompt input:

OpenMeshParamaterization.exe inputfile outputfile solver saveas

solver: 1.SparseLU, 2.BICGSTAB

saveas: 1.as 2D Vertex Coordinates, 2.as 2D Texture Coordinates

example: OpenMeshParamaterization.exe moser.off output.off 1 1

Screenshots:

![image](https://github.com/duoshengyu/MeshParamaterization/blob/master/screenshots/1.png)

![image](https://github.com/duoshengyu/MeshParamaterization/blob/master/screenshots/2.png)