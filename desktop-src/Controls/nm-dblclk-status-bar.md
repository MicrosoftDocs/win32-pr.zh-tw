---
title: 'NM_DBLCLK (狀態列) 通知碼 (Commctrl) '
description: 通知狀態列控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 4c02c76d-2bdb-48ef-aa8e-635d0e200eb1
keywords:
- NM_DBLCLK (的狀態列) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28866effbc4143dc9d0d5a3800f88711c99f88db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933915"
---
# <a name="nm_dblclk-status-bar-notification-code"></a>NM \_ DBLCLK (狀態列) 通知碼

通知狀態列控制項的父視窗，使用者在控制項內按兩下滑鼠左鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_DBLCLK
        
    LPNMMOUSE lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse)結構的指標，其中包含此通知的其他相關資訊。 **DwItemSpec** 成員包含已按下之區段的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 表示滑鼠按一下已處理，並隱藏系統的預設處理。 傳回 **FALSE** 以允許按一下的預設處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





