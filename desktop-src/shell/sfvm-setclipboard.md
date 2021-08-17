---
description: 當其中一個物件放在剪貼簿上作為功能表命令的結果時，就會通知 IShellView。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_SETCLIPBOARD 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99548be90c7f4fb9b840e4d4c6f816710c6e02cc1a888ce0c1c774f73c58f668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858210"
---
# <a name="sfvm_setclipboard-message"></a>SFVM \_ SETCLIPBOARD 訊息

當其中一個物件放在剪貼簿上作為功能表命令的結果時，就會通知 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 。 由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwEffect* \[在\]
</dt> <dd>

如果專案正在剪下到剪貼簿，請使用 (WPARAM) -2，如果正在將專案複製到剪貼簿，則為 (WPARAM) -3。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 




