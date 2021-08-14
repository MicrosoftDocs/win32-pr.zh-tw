---
title: 'PSN_QUERYINITIALFOCUS (Prsht.idl 的通知碼) '
description: 由屬性工作表傳送以提供屬性工作表頁面，有機會指定哪個對話方塊控制項應該接收初始焦點。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- PSN_QUERYINITIALFOCUS 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc82fe11893e728fbc9301868d9acdca5f7110bedfd37b4a16b473de0821f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169638"
---
# <a name="psn_queryinitialfocus-notification-code"></a>PSN \_ QUERYINITIALFOCUS 通知碼

由屬性工作表傳送以提供屬性工作表頁面，有機會指定哪個對話方塊控制項應該接收初始焦點。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify)結構的指標。 將此結構的 **lParam** 成員轉換成 **HWND** 型別，以抓取預設將會獲得焦點的控制項控點。 結構包含 [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構作為其第一個成員、 **hdr**。這個 **NMHDR** 結構的 **hwndFrom** 成員包含屬性工作表的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

若要指定哪個控制項應獲得焦點，請傳回控制項的控點。 否則，傳回零，焦點將會移至預設控制項。 若要設定傳回值，對話方塊程式必須使用 **DWL \_ MSGRESULT** 值來呼叫 [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)函數，並傳回 **TRUE**。

## <a name="remarks"></a>備註

處理此通知程式碼時，應用程式不能呼叫 [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) 函數。 傳回應取得焦點之控制項的控制碼，而屬性工作表管理員將會處理焦點變更。

\_如果屬性工作表管理員判斷頁面上沒有任何控制項應該取得焦點，則不會傳送 PSN QUERYINITIALFOCUS 通知碼。

此程式碼片段會針對 PSN QUERYINITIALFOCUS 執行簡單的處理常式 \_ 。 它會要求將初始焦點提供給 (**IDC \_ 位置**) 的位置控制項。

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> 使用 Aero wizard 樣式 ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) 時，不支援此通知碼。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Prsht.idl。h</dt> </dl> |



 

