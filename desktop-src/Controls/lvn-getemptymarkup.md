---
title: 'LVN_GETEMPTYMARKUP (Commctrl 的通知碼) '
description: 當控制項沒有專案時，由清單視圖控制項傳送至其父視窗。 LVN \_ GETEMPTYMARKUP 通知碼是要求父視窗提供標記文字。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 5ea74120-f347-493a-af14-6bda5b8f6082
keywords:
- LVN_GETEMPTYMARKUP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_GETEMPTYMARKUP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea693475ca42f962be07936f980cd3f5d52479c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844476"
---
# <a name="lvn_getemptymarkup-notification-code"></a>LVN \_ GETEMPTYMARKUP 通知碼

當控制項沒有專案時，由清單視圖控制項傳送至其父視窗。 LVN \_ GETEMPTYMARKUP 通知碼是要求父視窗提供標記文字。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_GETEMPTYMARKUP
        
    pnmMarkup = (NMLVEMPTYMARKUP*) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup)結構的指標。 設定此結構的成員，以提供清單視圖控制項的標記文字。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 表示在清單視圖控制項中設定標記文字，否則為 **FALSE** 。

## <a name="remarks"></a>備註

通知接收者會轉換 *lParam* 來取出 [**NMLVEMPTYMARKUP**](/windows/win32/api/commctrl/ns-commctrl-nmlvemptymarkup) 結構。 *WParam* 參數包含傳送此訊息之控制項的識別碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





