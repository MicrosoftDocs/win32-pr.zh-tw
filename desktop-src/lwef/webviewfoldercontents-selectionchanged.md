---
title: 'WebViewFolderContents. SelectionChanged 事件 (Shldisp .h) '
description: WebViewFolderContents. SelectionChanged 事件-在 view 中的任何專案或專案的選取狀態變更時，就會發生此事件。
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- SelectionChanged 事件舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- SelectionChanged
api_location:
- Shell32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cccabe52d7370d22fa086e9e8664163771062e8828c8ab2a6d016df30f13350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607828"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a>WebViewFolderContents. SelectionChanged 事件

發生于視圖中任何專案或專案的選取狀態變更時。

## <a name="syntax"></a>語法


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a>參數

此事件處理常式沒有參數。

## <a name="examples"></a>範例

下列範例示範如何適當地使用此事件，以供 HTML 中內嵌 JScript。


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectionChangedJ()
    {
        alert("SelectionChanged event was called");
    }
</script>

<script language="JavaScript" for="FileList" event="SelectionChanged">
    fnWebViewFolderContentsSelectionChangedJ();
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



 

 





