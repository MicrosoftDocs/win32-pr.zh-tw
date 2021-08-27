---
title: 'IPN_FIELDCHANGED (Commctrl 的通知碼) '
description: 當使用者變更控制項中的欄位，或從某個欄位移至另一個欄位時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 467cf7f14f3ff8d62f85d973e9a9d11c4dc6d20488ad5b7e30b4c0787b4b1a6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085548"
---
# <a name="ipn_fieldchanged-notification-code"></a>IPN \_ FIELDCHANGED 通知碼

當使用者變更控制項中的欄位，或從某個欄位移至另一個欄位時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress)結構的指標，其中包含已變更之位址的相關資訊。 此結構的 **iValue** 成員會包含輸入的值，即使超出欄位的範圍也一樣。 您可以將此成員修改為欄位範圍內的任何值，以回應此通知碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值會被忽略。

## <a name="remarks"></a>備註

此通知碼不會傳送以回應 [**IPM \_ SETADDRESS**](ipm-setaddress.md) 訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





