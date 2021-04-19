---
title: 'PSN_TRANSLATEACCELERATOR (Prsht.idl 的通知碼) '
description: 通知屬性工作表已收到鍵盤訊息。 它讓頁面有機會進行私用鍵盤快速鍵轉譯。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- PSN_TRANSLATEACCELERATOR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996174"
---
# <a name="psn_translateaccelerator-notification-code"></a>PSN \_ TRANSLATEACCELERATOR 通知碼

通知屬性工作表已收到鍵盤訊息。 它讓頁面有機會進行私用鍵盤快速鍵轉譯。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。 此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。**NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。 **PSHNOTIFY** 結構的 **lParam** 成員是訊息 [**訊息的指標。**](/windows/win32/api/winuser/ns-winuser-msg) 它可以轉換成 **LPMSG** 型別，以存取要轉譯之訊息的參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 PSNRET \_ MESSAGEHANDLED，表示不需要進一步處理。 傳回 PSNRET \_ >aad-userreadusingalternativesecurityid-noerror 以要求正常處理。

## <a name="remarks"></a>備註

若要設定傳回值，頁面的對話方塊程式必須使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數搭配 DWL \_ MSGRESULT 值。 對話方塊程式必須傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

