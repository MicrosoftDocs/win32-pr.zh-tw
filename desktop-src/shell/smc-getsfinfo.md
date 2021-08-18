---
description: 要求 Shell 資料夾功能表項目的相關資訊。
title: 'SMC_GETSFINFO 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4459670c-f0fd-4ae8-8a1f-810e1dcac713
api_name:
- SMC_GETSFINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ff74e59d0ef445a74d1141950b2b10e79ebce5502a02ec38c446bddc7317a885
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968077"
---
# <a name="smc_getsfinfo-message"></a>SMC \_ GETSFINFO 訊息

要求 Shell 資料夾功能表項目的相關資訊。


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*psminfo* 
</dt> <dd>

[**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo)結構的指標。 使用適當的資訊填入結構，並傳回 \_ [確定]。

</dd> </dl>

## <a name="return-value"></a>傳回值

返回 \_ [確定]。

## <a name="remarks"></a>備註

此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Shobjidl.h。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl.h .idl</dt> </dl> |



 

 




