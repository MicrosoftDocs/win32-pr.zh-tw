---
title: 'TVN_ENDLABELEDIT (Commctrl 的通知碼) '
description: 通知樹狀檢視控制項的父視窗，瞭解專案的標籤編輯結尾。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 82eb9fcd-de10-4efb-8501-78c5af5e089e
keywords:
- TVN_ENDLABELEDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TVN_ENDLABELEDIT
- TVN_ENDLABELEDITA
- TVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c30d494ad90b3d55f85b1ad154aed0f814a1eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103901"
---
# <a name="tvn_endlabeledit-notification-code"></a>IZDEBSKI \_ ENDLABELEDIT 通知碼

通知樹狀檢視控制項的父視窗，瞭解專案的標籤編輯結尾。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
TVN_ENDLABELEDIT 

    ptvdi = (LPNMTVDISPINFO) lParam 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMTVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmtvdispinfoa)結構的指標。 此結構的 **專案** 成員是 [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) 結構，其 **hItem**、 **lParam** 和 **pszText** 成員包含已編輯之專案的相關有效資訊。 如果已取消標籤編輯，則 **TVITEM** 結構的 **PszText** 成員為 **Null**;否則， **pszText** 是已編輯文字的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 **pszText** 成員為非 **Null**，則傳回 **TRUE** 將專案的標籤設定為已編輯的文字。 傳回 **FALSE** 以拒絕編輯過的文字，並還原為原始標籤。

## <a name="remarks"></a>備註

如果 **pszText** 成員為 **Null**，則會忽略傳回值。

如果您 \_ 為此專案指定了 LPSTR TEXTCALLBACK 值，而 **pszText** 成員為非 **Null**，則您 \_ 的 izdebski ENDLABELEDIT 處理常式應該將文字從 **pszText** 複製到本機儲存體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **Izdebski \_ENDLABELEDITW** (Unicode) 和 **izdebski \_ ENDLABELEDITA** (ANSI) <br/>         |



 

 





