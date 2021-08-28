---
title: 'HDN_ITEMCLICK (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，指出使用者已按一下控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 25ed0070-5891-4f36-9ae0-fc04e064401f
keywords:
- HDN_ITEMCLICK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMCLICK
- HDN_ITEMCLICKA
- HDN_ITEMCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe6bf01ed46d0294f654c21dc854933f0be04695f7edeee7a6849e23b01b027f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118006185"
---
# <a name="hdn_itemclick-notification-code"></a>HDN \_ ITEMCLICK 通知碼

通知標題控制項的父視窗，指出使用者已按一下控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_ITEMCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，該結構會識別標題控制項並指定已按下之標頭專案的索引，以及用來按一下專案的滑鼠按鍵。 **PItem** 成員會設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

標題控制項會在使用者放開滑鼠左鍵之後傳送此通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDN \_ITEMCLICKW** (Unicode) 和 **HDN \_ ITEMCLICKA** (ANSI) <br/>               |



 

 





