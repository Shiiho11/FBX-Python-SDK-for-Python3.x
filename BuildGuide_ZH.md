# 构建指南

## Note
关键就是使用的软件版本和官方指南里一样。  
运行程序可能需要管理员权限。

## Pre-requisites
+ Python
    + 下载并安装。将安装路径称为`<yourPythonPath>`。
+ Visual Studio 2015
    + 下载并安装。
+ FBX SDK
    + 下载并安装。将安装路径称为`<yourFBXSDKPath>`。<https://www.autodesk.com/products/fbx/overview> 点击 GET FBX SDKP
+ FBX Python Bindings
    + 下载并安装。将安装路径称为`<yourFBXPythonBindingsPath>`。<https://www.autodesk.com/products/fbx/overview> 点击 GET FBX SDK
+ Sip 4.19.3
    + 下载并解压。将解压后路径称为`<yourSipPath>`。<https://www.riverbankcomputing.com/software/sip/download/> 版本必须是4.19.3。

## 步骤

1. 移动FBX Python Bindings文件

    将`<yourFBXPythonBindingspath>\<version>`文件夹移动到路径较短的位置，例如`D:\2020.0.1`。因为较长的路径名可能会让Sip不能正常工作。将移动后的文件夹简称为`<yourBindingsPath>`。

2. 设置环境变量

    | | |  
    |-|-|
    | FBXSDK_ROOT | `<yourFBXSDKPath>\<version>` (例如: `D:\Program Files\Autodesk\FBX\FBX Python SDK\2020.0.1`) |
    | SIP_ROOT | `<yourSipPath>` (例如: `D:\sip-4.19.22`) |

3. 运行`PythonBindings.py`

    `PythonBindings.py`在`<yourBindingsPath>`中。不带arguments直接运行`PythonBindings.py`查看可用的选项。
    ```
    python PythonBindings.py
    ```
    结果:
    ```
    Syntax: PythonBindings.py module module [buildsip] [test] [doc]

        modules = Python2_x86 | Python2_ucs4_x86 | Python2_x64 | Python2_ucs4_x64 | Python3_x86 | Python3_x64 | Python2_ub | Python3_ub
    ```
    运行脚本:
    ```
    python PythonBindings.py <yourPythonVersion> buildsip
    ```
    例如:
    ```
    python PythonBindings.py Python3_x64 buildsip
    ```
    如果没有报错的话，恭喜您，成功了。
4. 使用FBX Python SDK

    构建完成的FBX Python SDK文件在`<yourBindingsPath>/build/Distrib/site-packages/fbx`中。应该包含有`fbx.pyd`、`FbxCommon.py`、`fbxsip.pyd`三个文件。复制文件到`<yourPythonPath>\Lib\site-packages`中。