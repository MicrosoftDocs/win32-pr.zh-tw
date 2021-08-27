---
title: 'TVN_BEGINLABELEDIT (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，瞭解專案的標籤編輯開始。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 67ed1f1f-7ccc-4e84-9540-4a46f6cd3a44
keywords:
- TVN_BEGINLABELEDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_BEGINLABELEDIT
- TVN_BEGINLABELEDITA
- TVN_BEGINLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8fdd2b75ee9f3dcc46e5449c275eeea141162f3d31f524b64e114a623bd915e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060088"
---
# <a name="tvn_beginlabeledit-notification-code"></a>IZDEBSKI \_ BEGINLABELEDIT 通知碼

通知樹狀檢視控制項的父視窗，瞭解專案的標籤編輯開始。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_BEGINLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa)結構的指標。 **專案** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema)結構，其中包含在 **hItem**、 **state**、 **lParam** 和 **pszText** 成員中編輯之專案的相關有效資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 表示取消標籤編輯。

## <a name="remarks"></a>備註

當標籤編輯開始時，會建立編輯控制項，但不會放置或顯示該控制項。 在顯示之前，樹狀檢視控制項會將 IZDEBSKI BEGINLABELEDIT 通知程式碼傳送至其父視窗 \_ 。

若要自訂標籤編輯，請執行 IZDEBSKI BEGINLABELEDIT 的處理常式， \_ 並讓它將 [**TVM \_ GETEDITCONTROL**](tvm-geteditcontrol.md) 訊息傳送至樹狀檢視控制項。 如果正在編輯標籤，傳回值將會是編輯控制項的控制碼。 您可以使用此控制碼來自訂編輯控制項，方法是傳送一般的 EM \_ XXX 訊息。

當使用者取消或完成編輯時，父視窗會收到 [izdebski \_ ENDLABELEDIT](tvn-endlabeledit.md) 通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_BEGINLABELEDITW** (Unicode) 和 **izdebski \_ BEGINLABELEDITA** (ANSI) <br/>     |



 

 





