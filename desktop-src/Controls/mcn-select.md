---
title: 'MCN_SELECT (Commctrl 的通知碼) '
description: 當使用者在月曆控制項中做出明確的日期選取時，由月曆控制項傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e71674ebccd9a896a92f701e65c7767866b64edac25208248f4683792b5261c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018966"
---
# <a name="mcn_select-notification-code"></a>MCN \_ 選取通知碼

當使用者在月曆控制項中做出明確的日期選取時，由月曆控制項傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
MCN_SELECT

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

**MCN \_ select** 通知碼類似于 [**MCN \_ SELCHANGE**](mcn-selchange.md)，但 **MCN \_ select** 只會傳送以回應使用者的明確日期選擇。 **MCN \_SELCHANGE** 適用于任何選取專案變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





