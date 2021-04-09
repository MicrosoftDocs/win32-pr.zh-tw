---
title: 'PSN_SETACTIVE (Prsht.idl 的通知碼) '
description: 通知頁面，指出即將啟用。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- PSN_SETACTIVE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934624"
---
# <a name="psn_setactive-notification-code"></a>PSN \_ advanced.field.setactive 通知碼

通知頁面，指出即將啟用。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。 此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。 **PSHNOTIFY** 結構的 **lParam** 成員不包含任何資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回零以接受啟用，或-1 表示要啟用下一個頁面或前一頁 (，取決於使用者按一下 [ **下一步]** 或 [ **上一頁** ] 按鈕) 。 若要將啟用設定為特定頁面，請傳回頁面的資源識別碼。

## <a name="remarks"></a>備註

PSN \_ advanced.field.setactive 通知碼會在頁面顯示之前傳送。 應用程式可以使用此通知碼來初始化頁面中的資料。

> [!Note]  
> 屬性工作表正在處理 \_ 傳送 PSN advanced.field.setactive 通知碼時的頁面清單。 在處理此通知程式碼時，請勿嘗試加入、移除或插入頁面。 這樣做會產生無法預期的結果。

 

若要設定傳回值，頁面的對話方塊程式必須使用 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數搭配 DWL \_ MSGRESULT 值，而且對話方塊程式必須傳回 **TRUE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

