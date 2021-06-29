## A PDF to word converter using Django

用于将pdf文件转换为word文件。网页为使用了BootStrap的响应式设计。

<img src="C:\Users\meranl\AppData\Roaming\Typora\typora-user-images\1624973848705.png" alt="1624973848705" style="zoom:50%;" />

### 主要结构

主项目目录：PDFconvert

APP目录：convert

前端页面：单个index，使用BootStrap+js+css实现前端设计；

<img src="C:\Users\meranl\AppData\Roaming\Typora\typora-user-images\1624974104216.png" alt="1624974104216" style="zoom: 67%;" />



### 核心程序

* 转换程序为`/convert/pypdf.py`，首先需要安装几个包，其中`pythoncom` 可`pip install pypiwin32` 安装，`pythoncom`通过`pip install pywin32`安装

```python
import tabula
import win32com.client
import os
import pythoncom
```

* 前端客户提交程序使用`convert/forms.py`，定义了上传表单：

```python
from django import forms
class UploadForm(forms.Form):
    uploadFile = forms.FileField()
    convertFormat = forms.CharField()
```







