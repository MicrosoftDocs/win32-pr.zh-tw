---
title: 'NM_RCLICK (] 索引標籤) 通知碼 (Commctrl) '
description: 通知索引標籤控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ef2270c0-eef3-4867-8aa3-b6ff7e1a5f0f
keywords:
- NM_RCLICK (] 索引標籤) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c74249e2c2984dd11dab7c4eab8147cb572f291
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025506"
---
# <a name="nm_rclick-tab-notification-code"></a>NM \_ RCLICK (tab) 通知碼

通知索引標籤控制項的父視窗，使用者在控制項內按一下滑鼠右鍵。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_RCLICK 

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回非零以允許預設處理，或零以允許預設處理。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





