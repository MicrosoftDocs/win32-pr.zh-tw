---
title: 'HDN_TRACK (Commctrl 的通知碼) '
description: 通知標題控制項的父視窗，表示使用者正在拖曳標題控制項中的分隔線。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- HDN_TRACK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fb32a553c85c8fb1bc8321dae5e85b3e7832cf90e4a6652ad163511ad4420d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435218"
---
# <a name="hdn_track-notification-code"></a>HDN \_ TRACK 通知碼

通知標題控制項的父視窗，表示使用者正在拖曳標題控制項中的分隔線。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera)結構的指標，其中包含標題控制項的相關資訊，以及正在拖曳其分割的專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **FALSE** 以繼續追蹤分隔線，或 **TRUE** 表示結束追蹤。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **HDN \_TRACKW** (Unicode) 和 **HDN \_ TRACKA** (ANSI) <br/>                       |



 

 





