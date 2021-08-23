---
title: 'WebViewFolderContents： Script 屬性 (Shldisp .h) '
description: 取得視圖的腳本物件。
ms.assetid: f65246c5-3cd6-43bd-b267-ad27bdd0b41e
keywords:
- 腳本屬性舊版 Windows 環境功能
- 腳本屬性舊版 Windows 環境功能，WebViewFolderContents 物件
- WebViewFolderContents 物件舊版 Windows 環境功能，腳本屬性
topic_type:
- apiref
api_name:
- WebViewFolderContents.Script
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d214719e2e40eaa680786188cf4815623d915c1e1e70e36f94eb80b6c4a6c25b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975448"
---
# <a name="webviewfoldercontentsscript-property"></a>WebViewFolderContents。 Script 屬性

取得視圖的腳本物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
objScript = WebViewFolderContents.Script
```



## <a name="property-value"></a>屬性值

[IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch)型別的變數，它會接收腳本物件。

## <a name="examples"></a>範例

下列範例示範如何在 JScript 內嵌于 HTML 中，適當使用此屬性。


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsScriptJ()
    {
        var objScript;

        objScript = FileList.Script;
        if (objScript != null)
        {
            alert(objScript.Name);
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
| 最低支援的用戶端<br/> | Windows 2000 Professional，僅 Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

