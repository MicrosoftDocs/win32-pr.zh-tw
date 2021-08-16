---
title: 'LVN_BEGINLABELEDIT (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，瞭解專案的標籤編輯開始。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: c13a9e95-22a9-476e-aeee-4928b8b096b0
keywords:
- LVN_BEGINLABELEDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_BEGINLABELEDIT
- LVN_BEGINLABELEDITA
- LVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab5b5ecfed8fdc15ec2779e204d01b0375c7da702e2a2e9fe8a3cdc3b178b0fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830649"
---
# <a name="lvn_beginlabeledit-notification-code"></a>LVN \_ BEGINLABELEDIT 通知碼

通知清單視圖控制項的父視窗，瞭解專案的標籤編輯開始。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_BEGINLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)結構的指標。 此結構的 **專案** 成員是 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構，其 **iItem** 成員會識別正在編輯的專案。 請注意，子無法編輯。 **iSubItem** 成員一律設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

若要允許使用者編輯標籤，請傳回 **FALSE**。

若要防止使用者編輯標籤，請傳回 **TRUE**。

## <a name="remarks"></a>備註

當標籤編輯開始時，會建立、定位和初始化編輯控制項。 在顯示之前，清單視圖控制項會將 LVN BEGINLABELEDIT 通知程式碼傳送給其父視窗 \_ 。

若要自訂標籤編輯，請執行 LVN BEGINLABELEDIT 的處理常式， \_ 並讓它將 [**LVM \_ GETEDITCONTROL**](lvm-geteditcontrol.md) 訊息傳送至清單視圖控制項。 如果正在編輯標籤，傳回值將會是編輯控制項的控制碼。 您可以使用此控制碼來自訂編輯控制項，方法是傳送一般的 **EM \_ XXX** 訊息。

當使用者取消或完成編輯時，父視窗會收到 [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) 通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVN \_BEGINLABELEDITW** (Unicode) 和 **LVN \_ BEGINLABELEDITA** (ANSI) <br/>     |



 

 





