---
description: 要求是否可以將資料物件放在隨附 SMDATA 結構所指定的專案上。
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: 'SMC_SFDDRESTRICTED 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973445"
---
# <a name="smc_sfddrestricted-message"></a>SMC \_ SFDDRESTRICTED 訊息

要求是否可以將資料物件放在隨附 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定的專案上。


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDropTarget* 
</dt> <dd>

Void 指標的位址，這個指標會接收 [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) 介面的指標。 如果您不想要接受資料物件，請將此值設定為 **Null** 。

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
| Idl<br/>                      | <dl> <dt>Shobjidl.h .idl</dt> </dl> |



 

 
