---
description: ShellFolderView. FocusedItem 屬性-取得代表具有輸入焦點之專案的 FolderItem 物件。
ms.assetid: ca88801d-c8fa-4c1c-9294-f52eada40ff6
title: 'ShellFolderView. FocusedItem 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.FocusedItem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 059a43ba0b727a8603ab87feea1e90ec1dd0105b1d17ab9bbf8d866a87a2b3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117676690"
---
# <a name="shellfolderviewfocuseditem-property"></a>ShellFolderView. FocusedItem 屬性

取得代表具有輸入焦點之專案的 [**FolderItem**](folderitem.md) 物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
objFocusedItem = ShellFolderView.FocusedItem
```



## <a name="property-value"></a>屬性值

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，可接收焦點的專案物件。

## <a name="remarks"></a>備註

**FocusedItem** 只能在本機系統上呼叫。 當透過 HTTP 或 UNC 在網頁上執行時，它將無法運作。

## <a name="examples"></a>範例

下列範例示範如何在 JScript 內嵌于 HTML 中，正確使用這個方法。


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFocusedItemJ()
    {
        var objFolderItem;
        
        objFolderItem = WebOC.Document.FocusedItem;
        if (objFolderItem != null)
        {
            alert("Got FolderItem object.");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=FocusedItem 
       type=button 
       value=FocusedItem 
       name=FocusedItem 
       onclick="fnShellFolderViewFocusedItemJ()">
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



 

 
