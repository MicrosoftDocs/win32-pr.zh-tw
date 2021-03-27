---
description: 通知回呼物件，使用者已叫用其中一個工具列或功能表命令。 由 IShellFolderViewCB：： MessageSFVCB 使用。
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: 'SFVM_INVOKECOMMAND 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852579"
---
# <a name="sfvm_invokecommand-message"></a>SFVM \_ INVOKECOMMAND 訊息

通知回呼物件，使用者已叫用其中一個工具列或功能表命令。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*idCmd* \[\]
</dt> <dd>

選定工具列或功能表項目的命令識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

此訊息基本上與傳統視窗程式中的 [**WM \_ 命令**](../menurc/wm-command.md) 訊息具有相同的功能。 它可讓回呼物件處理已加入 Windows 檔案總管工具或功能表列中的任何專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
