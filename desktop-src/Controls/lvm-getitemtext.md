---
title: 'LVM_GETITEMTEXT 訊息 (Commctrl .h) '
description: 抓取清單視圖專案或子專案的文字。 您可以明確地傳送此訊息，或使用 ListView \_ GetItemText 宏來傳送。
ms.assetid: 5711ed18-a766-4e7f-9e9d-b9203231b369
keywords:
- LVM_GETITEMTEXT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMTEXT
- LVM_GETITEMTEXTA
- LVM_GETITEMTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32d5292f9814b3ef62667d44582eab44a2f18ac6c274682d180dd26f1b7cdd9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062578"
---
# <a name="lvm_getitemtext-message"></a>LVM \_ GETITEMTEXT 訊息

抓取清單視圖專案或子專案的文字。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單視圖專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標。 若要取出專案文字，請將 **iSubItem** 設定為零。 若要取出子工作的文字，請將 **iSubItem** 設定為子索引。 **PszText** 成員指向接收文字的緩衝區。 **CchTextMax** 成員會指定緩衝區中的字元數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果您明確地傳送此訊息，它會傳回 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構之 **pszText** 成員中的字元數。

## <a name="remarks"></a>備註

您也可以藉由呼叫 [**ListView \_ GetItemText**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemtext) 宏來傳送此訊息。 不過，此宏不會傳回字串長度。

**LVM \_** [**Lvs) \_ OWNERDATA**](list-view-window-styles.md)樣式下不支援 GETITEMTEXT。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_GETITEMTEXTW** (Unicode) 和 **LVM \_ GETITEMTEXTA** (ANSI) <br/>           |



 

 





