---
description: 允許回呼物件在背景執行緒上要求列舉。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_BACKGROUNDENUM 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 724f971f52b57a008ec17ac316b78839a6890e3e2efee5d5a037ab4fdcd7ebf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592738"
---
# <a name="sfvm_backgroundenum-message"></a>SFVM \_ BACKGROUNDENUM 訊息

允許回呼物件在背景執行緒上要求列舉。 由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a>參數

此訊息沒有任何參數。

## <a name="remarks"></a>備註

回應此通知時，請返回 \_ [確定] 以啟用背景列舉。 根據預設，系統資料夾物件將會在列舉進行時顯示「停止顯示」動畫。 若要指定自訂動畫，請處理 [**SFVM \_ GETANIMATION**](sfvm-getanimation.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Shlobj.h。h</dt> </dl> |



 

 
