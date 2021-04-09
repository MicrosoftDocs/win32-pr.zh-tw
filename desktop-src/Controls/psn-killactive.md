---
title: 'PSN_KILLACTIVE (Prsht.idl 的通知碼) '
description: 通知頁面，因為正在啟用另一個頁面，或使用者已按下 [確定] 按鈕，所以即將遺失啟用。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- PSN_KILLACTIVE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934269"
---
# <a name="psn_killactive-notification-code"></a>PSN \_ KILLACTIVE 通知碼

通知頁面，因為正在啟用另一個頁面，或使用者已按下 [確定] 按鈕，所以即將遺失啟用。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。 此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。 **PSHNOTIFY** 結構的 **lParam** 成員不包含任何資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 以防止頁面遺失啟用，或傳回 **FALSE** 表示允許。

## <a name="remarks"></a>備註

應用程式會處理此通知碼，以驗證使用者輸入的資訊。

> [!Note]  
> 屬性工作表正在處理 \_ 傳送 PSN KILLACTIVE 通知碼時的頁面清單。 在處理此通知程式碼時，請勿嘗試加入、移除或插入頁面。 這樣做會產生無法預期的結果。

 

若要設定傳回值，頁面的對話方塊程式必須呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數，並將 DWL \_ MSGRESULT 值設定為傳回值。 對話方塊程式必須傳回 **TRUE**。

如果對話方塊程式將 DWL MSGRESULT 設 \_ 為 **TRUE**，它應該會顯示訊息方塊，以說明使用者的問題。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

