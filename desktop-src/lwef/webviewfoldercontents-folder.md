---
title: WebViewFolderContents.Folder 屬性 (Shldisp.h)
description: WebViewFolderContents 屬性-取得代表視圖的資料夾物件。
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- 資料夾屬性舊版 Windows 環境功能
- 資料夾屬性舊版 Windows 環境功能，WebViewFolderContents 物件
- WebViewFolderContents 物件舊版 Windows 環境功能，資料夾屬性
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e88fd7a54971fa088bdddbc78d3d8df4af610875
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102696"
---
# <a name="webviewfoldercontentsfolder-property"></a>WebViewFolderContents 資料夾屬性

取得代表視圖的 [**資料夾**](../shell/folder.md) 物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a>屬性值

接收 [**資料夾**](../shell/folder.md) 物件的物件。

## <a name="examples"></a>範例

下列範例示範如何在內嵌于 HTML 的 JScript 中，適當使用此屬性。


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

