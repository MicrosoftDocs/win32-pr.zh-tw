---
description: 通知回呼物件正在更新狀態列。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_UPDATESTATUSBAR 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f1bac364-1011-4308-8b9b-8ed1800dd30d
api_name:
- SFVM_UPDATESTATUSBAR
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 14045c797d7292099c1c7b2c67f5958609d8d6b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991630"
---
# <a name="sfvm_updatestatusbar-message"></a>SFVM \_ UPDATESTATUSBAR 訊息

通知回呼物件正在更新狀態列。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++
SFVM_UPDATESTATUSBAR 

    wParam = (WPARAM)(BOOL) fInitialize;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*fInitialize* \[在\]
</dt> <dd>

如果正在初始化狀態列，則 **布林** 值會設定為 **TRUE** 。

</dd> </dl>

## <a name="remarks"></a>備註

當您收到此通知時：

-   \_如果您將會處理更新，請返回 S。
-   Return \_ 會讓 HRESULT (嚴重性 \_ 成功，0，1) ，讓系統資料夾 view 物件設定狀態列文字。
-   Return E \_ 無法讓系統資料夾 view 物件處理狀態列。

預設狀態列文字如下所示。



| 狀態                      | 狀態列文字                         |
|-----------------------------|-----------------------------------------|
| 未選取任何專案           | \# \# 資料夾中的 "objects" ()           |
| 已選取一個專案           | 專案的提示（如果有的話）。 |
| 選取了一個以上的專案 | 「 \# \# 選取的物件」                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
