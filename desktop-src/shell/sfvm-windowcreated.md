---
description: 通知回呼物件正在建立資料夾檢視視窗。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_WINDOWCREATED 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2d09957e1164d5caacbddc23c9a72cb33ef80ffa156dd0538c0be1e24f192018
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111158"
---
# <a name="sfvm_windowcreated-message"></a>SFVM \_ WINDOWCREATED 訊息

通知回呼物件正在建立資料夾檢視視窗。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndView* \[在\]
</dt> <dd>

資料夾檢視的視窗控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
