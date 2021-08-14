---
title: 'PSN_APPLY (Prsht.idl 的通知碼) '
description: 傳送至屬性工作表中的每個頁面，表示使用者已按下 [確定]、[關閉] 或 [套用] 按鈕，並想要讓所有變更生效。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 18da6bdb-9409-49b6-8116-580fedd99a02
keywords:
- PSN_APPLY 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 522d4a0ea52f4cee495e689e8f0cdc91d7362ec3a1ee37ab81a911bc980d3209
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410034"
---
# <a name="psn_apply-notification-code"></a>PSN 套用 \_ 通知碼

傳送至屬性工作表中的每個頁面，表示使用者已按下 [確定]、[關閉] 或 [套用] 按鈕，並想要讓所有變更生效。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PSN_APPLY 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知程式碼的相關資訊，包括頁面的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

設定 PSNRET \_ >aad-userreadusingalternativesecurityid-noerror，表示對此頁面所做的變更有效且已套用。 如果所有頁面都設定 \_ 了 PSNRET >aad-userreadusingalternativesecurityid-noerror，則可以終結屬性工作表。 若要指出對此頁面所做的變更無效，以及防止屬性工作表終結，請設定下列其中一個傳回值：

-   PSNRET \_ 無效。 將不會終結屬性工作表，而且焦點將會傳回此頁面。
-   PSNRET \_ 無效 \_ 的 NOCHANGEPAGE。 將不會終結屬性工作表，而且焦點會在按下按鈕時，傳回具有焦點的頁面。

若要設定傳回值，頁面的對話方塊程式必須使用 DWL MSGRESULT 值來呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) 函數 \_ ，而且對話方塊程式必須傳回 **TRUE**。

## <a name="remarks"></a>備註

當使用者按一下 [確定]、[套用] 或 [關閉] 按鈕時，屬性工作表會將 [PSN \_ KILLACTIVE](psn-killactive.md) 通知傳送至使用中的頁面，讓它有機會驗證使用者的變更。 如果變更有效，屬性工作表會將 PSN 套用通知程式 \_ 代碼傳送至每個頁面，並將其導向以將新屬性套用至對應的專案。

> [!Note]  
> 當 \_ 傳送 PSN APPLY 通知碼時，屬性工作表正在處理頁面清單。 處理此通知時，請勿嘗試加入、移除或插入頁面。 這樣做會產生無法預期的結果。

 

如果使用者按一下 [確定] 按鈕， *lParam* 所指向之 [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的 **LParam** 成員會設定為 **TRUE** 。 如果已傳送 [**PSM \_ CANCELTOCLOSE**](psm-canceltoclose.md)訊息，且使用者按一下 [關閉] 按鈕，則也會將它設定為 **TRUE** 。 如果使用者按一下 [套用] 按鈕，則會設為 **FALSE** 。

[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。

處理此通知碼時，請勿呼叫 [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) 函數。

如果使用者按一下 [確定] 按鈕，而且每個頁面會傳回 PSNRET \_ >aad-userreadusingalternativesecurityid-noerror 值以回應 **PSN \_ APPLY**，則會終結模式屬性工作表。 如果有任何頁面傳回 \_ 不正確 PSNRET 或 PSNRET \_ 無效 \_ 的 NOCHANGEPAGE，則會立即取消套用的進程。 取消頁面之後的頁面不會收到 PSN 套用 \_ 通知碼。

若要接收此通知碼，頁面必須將 DWL \_ MSGRESULT 值設定為 **FALSE** ，以回應 [PSN \_ KILLACTIVE](psn-killactive.md) 通知碼。

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此通知碼。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

