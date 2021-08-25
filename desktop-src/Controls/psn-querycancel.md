---
title: 'PSN_QUERYCANCEL (Prsht.idl 的通知碼) '
description: 指出使用者已取消屬性工作表。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- PSN_QUERYCANCEL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff5ed6203d255a18c40044febb2f7afd9ab42e15c5a9d8ae9fa1a1a56518693
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798618"
---
# <a name="psn_querycancel-notification-code"></a>PSN \_ QUERYCANCEL 通知碼

指出使用者已取消屬性工作表。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。 此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。 **PSHNOTIFY** 結構的 **lParam** 成員不包含任何資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 以防止取消作業，或傳回 **FALSE** 以允許。

## <a name="remarks"></a>備註

當使用者按一下 [ **取消** ] 按鈕時，通常會傳送此通知碼。 當使用者按一下屬性工作表右上角的 [ **X** ] 按鈕或按下 esc 鍵時，也會一併傳送。 屬性工作表頁面可以處理此通知碼，要求使用者確認取消作業。

若要設定傳回值，頁面的對話方塊程式必須呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數，並 \_ 將 DWL MSGRESULT 設定為傳回值。 對話方塊程式必須傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

