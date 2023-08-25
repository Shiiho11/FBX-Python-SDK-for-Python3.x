# Build Guide

## Note
The key is to use the same software versions as mentioned in the official guide.  
Running the program might require administrator privileges.

## Pre-requisites
+ Python  
Download and install it. Refer to the installation path as`<yourPythonPath>`.
+ Visual Studio 2015  
Download and install it. It must be Visual Studio 2015.
+ FBX SDK VS2015  
Download and install it. Refer to the installation path as`<yourFBXSDKPath>`. Visit <https://www.autodesk.com/products/fbx/overview> and click on "GET FBX SDK" to download.
+ FBX Python Bindings  
Download and install it. Refer to the installation path as`<yourFBXPythonBindingsPath>`. Visit<https://www.autodesk.com/products/fbx/overview> and click on "GET FBX SDK" to download.
+ Sip 4.19.3  
Download and extract it. Refer to the extracted path as `<yourSipPath>`. Visit <https://www.riverbankcomputing.com/software/sip/download/> The version must be 4.19.3.

## Steps

1. Move FBX Python Bindings Files

    Move the `<yourFBXPythonBindingspath>\<version>` folder to a location with a shorter path, for example,`D:\2020.0.1`. Longer path names might cause issues with Sip. Abbreviate the moved folder as `<yourBindingsPath>`.

2. Set Environment Variables

    | | |  
    |-|-|
    | FBXSDK_ROOT | `<yourFBXSDKPath>\<version>` (e.g., `D:\Program Files\Autodesk\FBX\FBX Python SDK\2020.0.1`) |
    | SIP_ROOT | `<yourSipPath>` (e.g., `D:\sip-4.19.22`) |

3. Run `PythonBindings.py`

    `PythonBindings.py` is located in `<yourBindingsPath>`. Run `PythonBindings.py` without arguments to see available options.
    ```
    python PythonBindings.py
    ```
    Output:
    ```
    Syntax: PythonBindings.py module module [buildsip] [test] [doc]

        modules = Python2_x86 | Python2_ucs4_x86 | Python2_x64 | Python2_ucs4_x64 | Python3_x86 | Python3_x64 | Python2_ub | Python3_ub
    ```
    Run the script:
    ```
    python PythonBindings.py <yourPythonVersion> buildsip
    ```
    For example:
    ```
    python PythonBindings.py Python3_x64 buildsip
    ```
    If there are no errors, congratulations, you've succeeded.
4. Use FBX Python SDK

    The built FBX Python SDK files are located in `<yourBindingsPath>/build/Distrib/site-packages/fbx`. They should include `fbx.pyd`, `FbxCommon.py`, and `fbxsip.pyd`. Copy these files to `<yourPythonPath>\Lib\site-packages`.
