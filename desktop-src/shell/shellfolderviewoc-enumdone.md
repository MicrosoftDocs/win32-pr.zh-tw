---
description: 指出 ShellFolderView 物件已完成資料夾內容的列舉。
title: 'ShellFolderViewOC. EnumDone 事件 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: 00b0e58ed18ab0da9c3fa362da4b8e3e066cdcc4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841049"
---
# <a name="shellfolderviewocenumdone-event"></a>ShellFolderViewOC. EnumDone 事件

指出 [**ShellFolderView**](shellfolderview.md) 物件已完成資料夾內容的列舉。

## <a name="syntax"></a>語法


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a>參數

此事件處理常式沒有參數。

## <a name="remarks"></a>備註

[**ShellFolderView**](shellfolderview.md)物件必須先列舉資料夾的內容，才能加以顯示。 如果資料夾很大或位於遠端系統上，此程式可能需要數分鐘的時間。 在這段期間，會顯示動畫的空出圖，向使用者指出正在進行處理。 列舉完成之後，就會引發 **EnumDone** 事件，並以資料夾的內容取代下圖。

提供此事件的事件處理常式代碼，如下所示。


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ShellFolderViewOC**](shellfolderviewoc-object.md)
</dt> </dl>

 

 




