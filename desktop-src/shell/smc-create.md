---
description: 通知您已建立功能表區。
title: 'SMC_CREATE 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8eeca6f6-1718-4ff6-b4a7-4b68b9527468
api_name:
- SMC_CREATE
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 537c535d5470a691cf110b2217bb31cbfd0ad78b328f4fbb32a1445e0c5e6597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968217"
---
# <a name="smc_create-message"></a>SMC \_ 建立訊息

通知您已建立功能表區。


```C++
SMC_CREATE 
    lParam = (LPARAM) (LPSMDATA) psmd
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*psmd* 
</dt> <dd>

[**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata)結構的 **pvUserData** 成員指標。

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



 

 




