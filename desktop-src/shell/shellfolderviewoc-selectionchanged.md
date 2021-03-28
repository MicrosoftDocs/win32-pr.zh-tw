---
description: 指出視圖中一個或多個專案的選取狀態已變更。
title: 'ShellFolderViewOC. SelectionChanged 事件 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SelectionChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 85c37f4e-229f-4383-8218-10f8c2b0b8a0
ms.openlocfilehash: 3f88ad698b990847a9b7f2fa1b74cc5b53ec7beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320144"
---
# <a name="shellfolderviewocselectionchanged-event"></a>ShellFolderViewOC. SelectionChanged 事件

指出視圖中一個或多個專案的選取狀態已變更。

## <a name="syntax"></a>語法


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.SelectionChanged = EventHandler;
```



## <a name="parameters"></a>參數

此事件處理常式沒有參數。

## <a name="remarks"></a>備註

提供此事件的事件處理常式代碼，如下所示。


```
 
Private Sub object_SelectionChanged()
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

 

 




