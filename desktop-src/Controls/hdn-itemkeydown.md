---
title: 'HDN_ITEMKEYDOWN (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，已選取某個專案的按鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- HDN_ITEMKEYDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025481"
---
# <a name="hdn_itemkeydown-notification-code"></a>HDN \_ ITEMKEYDOWN 通知碼

通知標題控制項的父視窗，已選取某個專案的按鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含所按下之索引鍵的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





