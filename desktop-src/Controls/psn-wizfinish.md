---
title: 'PSN_WIZFINISH (Prsht.idl 的通知碼) '
description: 通知頁面，表示使用者已按一下嚮導中的 [完成] 按鈕。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 8ef0a8a7-2d25-4969-9b8f-e42dcc1c8fb5
keywords:
- PSN_WIZFINISH 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_WIZFINISH
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a11b018a57126c0882862271fa209fcd507224a46180ebb5fbaed4355fc040
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588178"
---
# <a name="psn_wizfinish-notification-code"></a>PSN \_ WIZFINISH 通知碼

通知頁面，表示使用者已按一下嚮導中的 [ **完成]** 按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PSN_WIZFINISH 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。 此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。 **PSHNOTIFY** 結構的 **lParam** 成員不包含任何資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

-   傳回 **TRUE** 以防止嚮導完成。
-   [版本5.80。](common-control-versions.md) 及更新版本。 傳回視窗控制碼，以防止嚮導完成。 Wizard 會將焦點設為該視窗。 視窗必須由 wizard 頁面擁有。
-   傳回 **FALSE** 以允許嚮導完成。

## <a name="remarks"></a>備註

若要設定傳回值，頁面的對話方塊程式必須使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數搭配 DWL \_ MSGRESULT 值，而且對話方塊程式必須傳回 **TRUE**。

[版本5.80。](common-control-versions.md) 如果您的應用程式傳回 **TRUE** 以防止嚮導完成，則無法控制頁面上的哪個視窗會獲得焦點。 需要停止完成嚮導的應用程式通常應該會在取得焦點的 wizard 頁面上傳回視窗控制碼來完成這項作業。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

