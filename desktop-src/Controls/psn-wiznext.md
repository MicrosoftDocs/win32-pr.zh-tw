---
title: 'PSN_WIZNEXT (Prsht.idl 的通知碼) '
description: 通知頁面，表示使用者已按下 wizard 中的 [下一步] 按鈕。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ff5be154-f2d1-403d-8f22-8f6cacfb66b1
keywords:
- PSN_WIZNEXT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_WIZNEXT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 145591b725548ffc4175541fd37db8f285533590
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106993750"
---
# <a name="psn_wiznext-notification-code"></a>PSN \_ WIZNEXT 通知碼

通知頁面，表示使用者已按下 wizard 中的 [ **下一步** ] 按鈕。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PSN_WIZNEXT 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標，其中包含通知碼的相關資訊。 此結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。 **PSHNOTIFY** 結構的 **lParam** 成員不包含任何資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回0以允許 wizard 移至下一個頁面。 傳回-1，以防止嚮導變更頁面。 若要顯示特定頁面，請傳回其對話資源識別碼。 如果使用 [**PSP \_ DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) 旗標來指定對話方塊，此通知會傳回對話方塊範本的指標。

## <a name="remarks"></a>備註

若要設定傳回值，頁面的對話方塊程式必須使用 **DWL \_ MSGRESULT** 值來呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數，並傳回 **TRUE**。 例如：

``` syntax
case PSN_WIZNEXT :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZBACK :
    ...
```

> [!Note]  
> 屬性工作表正在處理 \_ 傳送 PSN WIZNEXT 通知碼時的頁面清單。 您可以新增、插入或移除頁面以回應這些通知碼，但如果您在目前頁面之前插入或移除頁面，就必須特別小心。

 

如果您插入或移除目前頁面之前的頁面，您必須透過 **DWL \_ MSGRESULT** 傳回 () 非零值，以指定所需的新頁面。 但是請注意，如果您插入或移除目前頁面之前的頁面 (，其索引小於目前的頁面) ， [PSN \_ KILLACTIVE](psn-killactive.md) 可能會傳送至錯誤的頁面。

基於這個理由，建議在回應 PSN WIZNEXT 和 PSN WIZBACK 的情況下，動態新增和移除頁面的程式， \_ 只對清單結尾的頁面這麼 [ \_ ](psn-wizback.md) 做。 如果您想要讓您的嚮導正確地移除頁面，請將動態頁面保留在清單結尾，然後跳回永久頁面，然後再加以刪除。

例如，假設 wizard 包含一個簡介頁面、一系列的動態頁面和一個完成頁面，而且您想要在使用者到達完成頁面時刪除動態頁面。

1.  Wizard 會從兩個頁面開始：「簡介」和「完成」。 使用者會在 [簡介] 頁面上開始。
    1.   (使用者的簡介) 
    2.  Completion
2.  當使用者離開 [簡介] 時，嚮導會新增動態頁面，並將使用者放在第一個動態頁面，方法是透過 **DWL \_ MSGRESULT** 傳回 (，) [動態 1] 頁面的對話識別碼。 在此範例中，有三個動態頁面。
    1.  簡介
    2.  Completion
    3.  動態 1 (使用者在此) 
    4.  動態2
    5.  動態3
3.  當使用者流覽動態頁面至「動態3」，然後流覽至下一個頁面之後，應用程式應該將使用者放在頁面「完成」。 同樣地，這是透過 **DWL \_ MSGRESULT** 傳回 (，) [完成] 頁面的對話方塊識別碼來完成。
    1.  簡介
    2.   (使用者的完成) 
    3.  動態1
    4.  動態2
    5.  動態3
4.  然後，應用程式可以將三個動態頁面 (編號的三至五) 安全地移除。
    1.  簡介
    2.   (使用者的完成) 

請注意，只有在您的 wizard 動態移除頁面時，才需要這項技術。 如果您的 wizard 只動態新增頁面，則不需要此程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

