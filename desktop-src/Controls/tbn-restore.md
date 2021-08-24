---
title: 'TBN_RESTORE (Commctrl 的通知碼) '
description: 通知工具列的父視窗正在還原工具列。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b1f0c801-d56b-4e93-b9ba-b572aaa38647
keywords:
- TBN_RESTORE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_RESTORE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f267e5cff52eb1a6011b16aa02d63870503478051e72d574da05467c8329f91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119543497"
---
# <a name="tbn_restore-notification-code"></a>TBN \_ 還原通知碼

通知工具列的父視窗正在還原工具列。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TBN_RESTORE 

    lpnmtb = (LPNMTBRESTORE) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTBRESTORE**](/windows/win32/api/commctrl/ns-commctrl-nmtbrestore)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

應用程式應該會傳回零以回應還原程式開始時所收到的第一個 **TBN \_ 還原** 通知程式碼，以繼續還原按鈕資訊。 如果應用程式傳回非零值，則還原進程會取消。

## <a name="remarks"></a>備註

應用程式會在一開始還原程式時，每個按鈕一次收到此通知碼。 此通知碼讓您有機會從先前儲存的資料流程中解壓縮資訊。 如果您尚未儲存任何資訊，請忽略通知碼。 如需如何處理 **TBN \_ 還原** 的詳細討論，請參閱 [工具列自訂](toolbar-controls-overview.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





