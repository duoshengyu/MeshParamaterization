# If the text is garbled, please convert encoding to UTF-8.
# MeshParamaterization
メッシュパラメータ化の実装です。
[Mesh Parameterization Methods and Their Applications Chapter 3 Alla Sheffer .al.2006]

実行ファイル：Release/OpenMeshParamaterization.exe

*実行環境等を含めた実行方法:

動作確認：Windows 10　Visual Studio 2013

開発時間と人数:  一年前　一周　一人

開発言語：C++ OpenGL

外部ライブラリ：glfw glew Openmesh Eigen

実行方法："OpenGL.sln"　Visual Studio 2013で開けたら、F5を押す。

使用条件：1. *.off ファイル　2.境界をついたメッシュ　
操作方法：
コマンド・プロンプト中で、OpenMeshParamaterization.exeのいるフォルダにcd.

OpenMeshParamaterization　インプットファイルの名前　アウトプットファイルの名前　ソルバー(1 or 2)　アウトプットタイプ(1 or 2)

ソルバー　1.SparseLU, 2.BICGSTAB

アウトプットタイプ　1.as 2D Vertex Coordinates, 2.as 2D Texture Coordinates

*プログラムを作成する上で苦労した箇所は？

デバッグ、メッシュパラメータ化の勉強

*力をいれて作った部分で、「プログラム上」で特に注意してみてもらいたい箇所は？

common/OMmodel.cppのBoundaryMap関数、境界の頂点は2Dの正方形にマッピング。

common/OMmodel.cppのSolve関数、他の頂点の座標を計算するための連立一次方程式の取り込み。

*参考にしたソースファイルがあるなら、どの様なところを参考にしましたか？またその部分のファイル名を書いてください

なし

*他人のコードと関数：

なし



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

![image](https://github.com/duoshengyu/MeshParamaterization/blob/master/screenshots/1.PNG)

![image](https://github.com/duoshengyu/MeshParamaterization/blob/master/screenshots/2.PNG)
