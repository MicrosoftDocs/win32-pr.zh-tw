---
title: 'TRBN_THUMBPOSCHANGING (Commctrl 的通知碼) '
description: 通知正在進行的捲軸位置變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23722b68f28a5157948ac6277858193366242fe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103945901"
---
# <a name="trbn_thumbposchanging-notification-code"></a>TRBN \_ THUMBPOSCHANGING 通知碼

通知正在進行的捲軸位置變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTRBTHUMBPOSCHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging)結構的指標。 呼叫端負責配置此結構並設定其成員，包括包含之 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) 結構的成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 以防止捲動方塊移至指定的位置。

## <a name="remarks"></a>備註

將此通知傳送給未接聽 [**wm \_ HSCROLL**](wm-hscroll.md) 或 [**WM \_ VSCROLL**](wm-vscroll.md) 訊息的用戶端。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





