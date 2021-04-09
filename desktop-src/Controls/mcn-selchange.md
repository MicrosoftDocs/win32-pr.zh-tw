---
title: 'MCN_SELCHANGE (Commctrl 的通知碼) '
description: 月曆控制項在目前選取日期或日期範圍變更時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- MCN_SELCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024728"
---
# <a name="mcn_selchange-notification-code"></a>MCN \_ SELCHANGE 通知碼

月曆控制項在目前選取日期或日期範圍變更時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange)結構的指標，其中包含目前所選取日期範圍的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

例如， \_ 當使用者在目前月份內明確變更選取範圍，或在回應下一個/上一個月導覽時，以隱含方式變更選取範圍時，控制項會傳送 MCN SELCHANGE。 系統也會定期傳送此通知碼，讓控制項可以回應日期變更。

此通知碼類似于 [MCN \_ SELECT](mcn-select.md)，但會傳送以回應任何選取專案的變更。 MCN \_ SELECT 只傳送給明確的日期選擇。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





