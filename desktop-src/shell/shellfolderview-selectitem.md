---
description: ShellFolderView. SelectItem 方法-在 view 中設定專案的選取狀態。
title: 'ShellFolderView. SelectItem 方法 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: c8cbff0da4da55d9621bfeb01f26c5ed62fe230a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116746"
---
# <a name="shellfolderviewselectitem-method"></a>ShellFolderView. SelectItem 方法

在視圖中設定專案的選取狀態。

## <a name="syntax"></a>語法


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*vItem* \[在\]
</dt> <dd>

類型： **Variant \***

將設定選取狀態的 [**FolderItem**](folderitem.md) 物件。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

類型： **整數**

一組旗標，表示新的選取狀態。 這可以是下列其中一個或多個值。

<dt>



  (0)


</dt> <dd>

取消選取專案。

</dd> <dt>



 (1)


</dt> <dd>

選取專案。

</dd> <dt>



 (3)


</dt> <dd>

將專案放在編輯模式中。

</dd> <dt>



 (4)


</dt> <dd>

取消選取指定的專案以外的所有專案。

</dd> <dt>



 (8)


</dt> <dd>

確定專案顯示在視圖中。

</dd> <dt>



 (16)


</dt> <dd>

將焦點提供給專案。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

[**FocusedItem**](shellfolderview-focuseditem.md) 只能在本機系統上呼叫。 當透過 HTTP 或 UNC 在網頁上執行時，它將無法運作。

## <a name="examples"></a>範例

下列範例示範如何在內嵌于 HTML 的 JScript 中正確使用這個方法。


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
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
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
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



 

 




