---
title: 'LVN_ENDLABELEDIT (Commctrl 的通知碼) '
description: 通知清單視圖控制項的父視窗，瞭解專案的標籤編輯結尾。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 03129fef-abf1-4374-b4b8-503c46ef7115
keywords:
- LVN_ENDLABELEDIT 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ENDLABELEDIT
- LVN_ENDLABELEDITA
- LVN_ENDLABELEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a33ab69a04202aeb3817d3eeadf01fb6f1fcaac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965540"
---
# <a name="lvn_endlabeledit-notification-code"></a>LVN \_ ENDLABELEDIT 通知碼

通知清單視圖控制項的父視窗，瞭解專案的標籤編輯結尾。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。


```C++
LVN_ENDLABELEDIT

    pdi = (LPNMLVDISPINFO) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa)結構的指標。 此結構的 **專案** 成員是 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構，其 **iItem** 成員會識別正在編輯的專案。 當傳送 LVN ENDLABELEDIT 通知碼時，**專案** 的 **pszText** 成員會包含有效的值 \_ ，不論 LVIF \_ 文字旗標是否在 **LVITEM** 結構的 **mask** 成員中設定。 如果使用者取消編輯， **LVITEM** 結構的 **pszText** 成員會是 **Null**;否則， **pszText** 是已編輯文字的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **pszText** 成員為非 **Null**，則傳回 **TRUE** 將專案的標籤設定為已編輯的文字。 傳回 **FALSE** 以拒絕編輯過的文字，並還原為原始標籤。

如果 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的 **PszText** 成員是 **Null**，則會忽略傳回值。

## <a name="remarks"></a>備註

對話程式的傳回值就是是否已處理訊息。 第二個傳回值必須藉由使用 **DWLP_MSGRESULT** 呼叫 [**SetwindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)來設定。

當使用者開始編輯專案標籤時，清單視圖控制項的父視窗會收到 [LVN \_ BEGINLABELEDIT](lvn-beginlabeledit.md) 通知碼。 當使用者取消或完成編輯時，父視窗會收到 LVN \_ ENDLABELEDIT 通知碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVN \_ENDLABELEDITW** (Unicode) 和 **LVN \_ ENDLABELEDITA** (ANSI) <br/>         |



 

 





