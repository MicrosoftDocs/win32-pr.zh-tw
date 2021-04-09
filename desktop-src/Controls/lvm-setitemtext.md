---
title: 'LVM_SETITEMTEXT 訊息 (Commctrl .h) '
description: 變更清單視圖專案或子專案的文字。 您可以明確地傳送此訊息，或使用 ListView \_ SetItemText 宏來傳送。
ms.assetid: 1a9c7e4d-78e0-44c7-bf4f-d0fc7a0049f3
keywords:
- LVM_SETITEMTEXT message Windows 控制項
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
ms.openlocfilehash: d326e48047325fc9aff2c6607da6d7d377965adf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843664"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_SETITEMTEXTW** (Unicode) 和 **LVM \_ SETITEMTEXTA** (ANSI) <br/>           |



 

 





