---
title: 'HDN_ITEMCHANGING (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，標題專案的屬性即將變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- HDN_ITEMCHANGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843148"
---
# <a name="hdn_itemchanging-notification-code"></a>HDN \_ ITEMCHANGING 通知碼

通知標題控制項的父視窗，標題專案的屬性即將變更。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項和標頭專案的相關資訊，包括即將變更的屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **FALSE** 表示允許變更，或 **TRUE** 表示防止這些變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDN \_ITEMCHANGINGW** (Unicode) 和 **HDN \_ ITEMCHANGINGA** (ANSI) <br/>         |



 

 





