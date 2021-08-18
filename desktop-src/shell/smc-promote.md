---
description: 升級隨附的 SMDATA 結構所指定的專案。
title: 'SMC_PROMOTE 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b1208673-06b4-42b2-b4ac-872fd22927df
api_name:
- SMC_PROMOTE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a82c172d340bd4e03f7361ae3129294f3e778b221e45e0f22d8baef2a0d70a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968017"
---
# <a name="smc_promote-message"></a>SMC \_ 升階訊息

升級隨附的 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定的專案。


```C++
SMC_PROMOTE
```



## <a name="parameters"></a>參數

此訊息沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 S \_ OK。

## <a name="remarks"></a>備註

此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Shobjidl.h。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl.h .idl</dt> </dl> |



 

 




