---
title: 'TTN_SHOW (Commctrl 的通知碼) '
description: 通知擁有者視窗即將顯示工具提示控制項。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ddfd18cd-0681-4e4a-b258-873f98da7479
keywords:
- TTN_SHOW 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TTN_SHOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74397223f20668487e78cea15e2e1507026ee65089e5011065b3f177514e899b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408810"
---
# <a name="ttn_show-notification-code"></a>TTN \_ 顯示通知碼

通知擁有者視窗即將顯示工具提示控制項。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TTN_SHOW

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

[版本 4.70](common-control-versions.md)。 若要將工具提示顯示在其預設位置，請傳回零。 若要自訂工具提示位置，請使用 [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) 函式重新置放工具提示視窗，並傳回 **TRUE**。

> [!Note]  
> 若為4.70 之前的版本，則不會傳回值。

 

## <a name="remarks"></a>備註

工具提示視窗矩形會比其文字顯示矩形稍微大一點，且其原點會向上和向左位移。 如果您需要精確地定位工具提示的文字顯示矩形， [**TTM \_ ADJUSTRECT**](ttm-adjustrect.md) 訊息會將文字顯示矩形轉換成對應的工具提示視窗矩形，反之亦然。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

