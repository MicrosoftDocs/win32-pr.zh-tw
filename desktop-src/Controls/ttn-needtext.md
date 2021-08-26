---
title: 'TTN_NEEDTEXT (Commctrl 的通知碼) '
description: 由工具提示控制項傳送，以取得顯示工具提示視窗所需的資訊。 此通知碼與 TTN GETDISPINFO 相同 \_ 。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dae1ac1eb721d918acf38745f19c7e6dee4a6a296c7fa8003f516717ece6cf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119967798"
---
# <a name="ttn_needtext-notification-code"></a>TTN \_ NEEDTEXT 通知碼

由工具提示控制項傳送，以取得顯示工具提示視窗所需的資訊。 此通知碼與 [TTN \_ GETDISPINFO](ttn-getdispinfo.md)相同。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)結構的指標，此結構會識別需要文字的工具，並接收要求的資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此通知的傳回值。

## <a name="remarks"></a>備註

填妥結構適當的成員，以將要求的資訊傳回給工具提示控制項。 如果您的訊息處理常式將 [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa)結構的 **uFlags** 成員設定為 TTF \_ DI \_ SETITEM，則工具提示控制項會儲存資訊，而不會再次要求它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **TTN \_NEEDTEXTW** (Unicode) 和 **TTN \_ NEEDTEXTA** (ANSI) <br/>                 |



 

 





