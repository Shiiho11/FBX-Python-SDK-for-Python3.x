# FBX Python SDK for Python3.x
language: English / 中文(Chinese)

The FBX Python SDK provided by Autodesk only supports Python2.7 and python3.3. In order to use the FBX Python SDK in Python3.7, I downloaded the FBX Python bindings and tried to build it. As a result, I encountered many errors. So I'm here to share the FBX Python SDK that has been built and provide a more detailed build guide.

Autodesk提供的FBX Python SDK只支持Python2.7和Python3.3。为了能在Python3.7使用FBX Python SDK，我下载了FBX Python Bindings并试图构建，结果遇到了非常多错误。所以我在此分享构建完成的FBX Python SDK，并提供更详细的构建指南。

## Using the FBX Python SDK / 使用FBX Python SDK
Copy the contents in `<SDKVersion_PythonVersion>` to `<yourPythonPath>\Lib\site-packages`.  
Note: I only built the FBX Python SDK 2020.0.1 for Python3.7.6_x64/Python3.8.3_x64, there is no guarantee that other versions can be used normally.

将`<SDKVersion_PythonVersion>`中的内容复制到`<yourPythonPath>\Lib\site-packages`中。  
Note: 我只构建了用于Python3.7.6_x64/Python3.8.3_x64的FBX Python SDK 2020.0.1，不保证其他版本可以正常使用。

## Build FBX Python SDK for any Python version / 构建适用于任意Python版本的FBX Python SDK
Please read the building guide: BuildGuide_EN.md / BuildGuide_ZH.md

请阅读构建指南: BuildGuide_EN.md / BuildGuide_ZH.md
