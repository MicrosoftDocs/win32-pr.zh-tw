---
description: 針對伴隨的 SMDATA 結構所指定的專案，要求有燕號提示的標題和文字。
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: 'SMC_CHEVRONGETTIP 訊息 (Shobjidl.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e64636994743d4b13a96fe75947fb515c4dbd3edcc94e6dee0fa85efb8bc9d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968237"
---
# <a name="smc_chevrongettip-message"></a>SMC \_ CHEVRONGETTIP 訊息

針對伴隨的 [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) 結構所指定的專案，要求有燕號提示的標題和文字。


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszTipTitle* 
</dt> <dd>

緩衝區的指標，此緩衝區會接收以 **Null** 終止的 Unicode 字串，其中包含提示的標題。 這個字串的長度不能超過最大 \_ 路徑字元，包括結束的 **Null** 字元。

</dd> <dt>

*pwszTipText* 
</dt> <dd>

緩衝區的指標，此緩衝區會接收以 **Null** 終止的 Unicode 字串，其中包含內容提示的文字。 這個字串的長度不能超過最大 \_ 路徑字元，包括結束的 **Null** 字元。

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



 

 




