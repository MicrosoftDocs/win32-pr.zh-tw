---
title: 'PSN_RESET (Prsht.idl 的通知碼) '
description: 通知頁面：即將終結屬性工作表。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- PSN_RESET 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb9f14b037d8757469497e644d870a887e6db36172b171f31b00d5615ff39532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409809"
---
# <a name="psn_reset-notification-code"></a>PSN \_ 重設通知碼

通知頁面：即將終結屬性工作表。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

自從上一個 PSN 套用通知碼之後所做的所有變更都已取消，但在 [**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)的情況下則不支援該通知碼。 [ \_](psn-apply.md)

如果使用者按一下屬性工作表右上角的 [ **X** ] 按鈕， *lParam* 所指向之 [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的 **lParam** 成員將設定為 **TRUE** 。 如果使用者按一下 [**取消**] 按鈕，就會是 **FALSE** 。 **PSHNOTIFY** 結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。

應用程式可以使用此通知碼作為執行清除作業的機會。

> [!Note]  
> 在 \_ 傳送 PSN 重設通知碼時，屬性工作表正在處理頁面清單。 在處理此通知程式碼時，請勿嘗試加入、移除或插入頁面。 這樣做會產生無法預期的結果。

 

處理此通知碼時，請勿呼叫 [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

