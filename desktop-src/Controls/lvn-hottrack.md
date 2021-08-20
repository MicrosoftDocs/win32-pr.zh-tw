---
title: 'LVN_HOTTRACK (Commctrl 的通知碼) '
description: 當使用者將滑鼠移到專案上時，由清單視圖控制項所傳送。 只有具有 LVS) \_ EX \_ TRACKSELECT 擴充清單視圖樣式的清單視圖控制項才會傳送此通知碼。 它是以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 6bbfe6b8-9b67-49e4-9481-65abe98608bb
keywords:
- LVN_HOTTRACK 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_HOTTRACK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab311b17f287b695a6b21d333f7183fdda272029e2c57dfe468527d765d1602
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830429"
---
# <a name="lvn_hottrack-notification-code"></a>LVN \_ HOTTRACK 通知碼

當使用者將滑鼠移到專案上時，由清單視圖控制項所傳送。 只有具有 [**lvs) \_ EX \_ TRACKSELECT**](extended-list-view-styles.md) 擴充清單視圖樣式的清單視圖控制項才會傳送此通知碼。 它是以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_HOTTRACK

    lpnmlv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLISTVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview)結構的指標，其中包含此通知碼的相關資訊。 此結構的 **iItem**、 **iSubItem** 和 **ptAction** 成員包含專案的相關資訊。 接收應用程式可以修改 **iItem** 成員，以指定將選取的專案。 如果 **iItem** 設為-1，則不會選取任何專案。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零以允許清單視圖執行其一般追蹤選取處理。 如果應用程式傳回非零值，則不會選取該專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





