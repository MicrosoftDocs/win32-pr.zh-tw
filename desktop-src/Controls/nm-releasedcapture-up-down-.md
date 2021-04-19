---
title: 'NM_RELEASEDCAPTURE () 通知程式碼 (Commctrl) '
description: 通知上下控制項的父視窗，控制項正在釋放滑鼠捕捉。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 88a4a9a2-ba7f-4ccc-b5bf-749f49dc666b
keywords:
- NM_RELEASEDCAPTURE () 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b94f2a61727861cbf47720a41c7255763992b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969188"
---
# <a name="nm_releasedcapture-up-down-notification-code"></a>NM \_ RELEASEDCAPTURE () 通知碼

通知上下控制項的父視窗，控制項正在釋放滑鼠捕捉。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

控制項會忽略此通知碼的傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





