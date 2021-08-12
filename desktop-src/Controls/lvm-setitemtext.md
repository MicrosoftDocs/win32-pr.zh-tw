---
title: 'LVM_SETITEMTEXT 訊息 (Commctrl .h) '
description: 變更清單視圖專案或子專案的文字。 您可以明確地傳送此訊息，或使用 ListView \_ SetItemText 宏來傳送。
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMTEXT
- LVM_SETITEMTEXTA
- LVM_SETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14eb5ddcff18a84f93febb22ef6661d8871df9b5578cc79f071b6e51b557c87b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670871"
---
# <a name="lvm_setitemtext-message"></a>LVM \_ SETITEMTEXT 訊息

變更清單視圖專案或子專案的文字。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemtext) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單視圖專案的以零為起始的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標。 **ISubItem** 成員是子專案的索引，或者可以是零來設定專案標籤。 **PszText** 成員是以 null 終止之字串的位址，其中包含新的文字;它也可以是 **Null**。 **PszText** 成員也可以是 LPSTR \_ TEXTCALLBACK，以表示父視窗儲存文字的回撥專案。 在此情況下，清單視圖控制項會在需要文字時，傳送 [**LVN \_ GETDISPINFO**](lvn-getdispinfo.md) 通知碼給父系。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果您明確傳送此訊息，則會在成功時傳回 **TRUE** ，否則會傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_SETITEMTEXTW** (Unicode) 和 **LVM \_ SETITEMTEXTA** (ANSI) <br/>           |



 

 





