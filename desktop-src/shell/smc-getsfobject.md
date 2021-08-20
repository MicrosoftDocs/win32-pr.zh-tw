---
description: SMC_GETSFOBJECT 訊息-要求指定物件的指標。
title: 'SMC_GETSFOBJECT 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0b0b5e9e170c9df4bd89279f2b96c80a76002ba2adbbe14ebd90afe458ece161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047070"
---
# <a name="smc_getsfobject-message"></a>SMC \_ GETSFOBJECT 訊息

要求指定物件的指標。


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Iid* 
</dt> <dd>

與要求的物件相關聯的 IID。

</dd> <dt>

*光伏* 
</dt> <dd>

將指標接收至所要求介面的 void 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

返回 \_ [確定]。

## <a name="remarks"></a>備註

此通知是由 [**IShellMenuCallback：： CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) 方法所接收。 它類似于 [**SMC \_ GETOBJECT**](smc-getobject.md) ，但用於 Shell 資料夾專案。 建立要求的物件，並將指標指派給所要求的介面，以做為 *pv*。

可能會要求下列介面。

-   [**IStream**](/windows/win32/api/objidl/nn-objidl-istream)
-   [**IShellMenu**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [**IShellMenuCallback**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Shobjidl.h。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shobjidl.h .idl</dt> </dl> |



 

 
