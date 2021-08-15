---
title: 'LVM_SETCOLUMN 訊息 (Commctrl .h) '
description: 設定清單視圖資料行的屬性。 您可以明確地傳送此訊息，或使用 ListView \_ SetColumn 宏來傳送。
ms.assetid: 8ca1c269-fd86-4561-940d-b75f8ca2b731
keywords:
- LVM_SETCOLUMN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETCOLUMN
- LVM_SETCOLUMNW
- LVM_SETCOLUMNW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cca00e62d941a753c70e0dd31c1af4003fe639d49503be7009fe5a010febf0c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019216"
---
# <a name="lvm_setcolumn-message"></a>LVM \_ SETCOLUMN 訊息

設定清單視圖資料行的屬性。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumn) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

資料行的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)結構的指標，其中包含新的資料行屬性。 **遮罩** 成員會指定要設定的資料行屬性。 如果 **遮罩** 成員指定 LVCF \_ 文字值，則 **pszText** 成員是以 null 結束之字串的位址，而且會忽略 **cchTextMax** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_SETCOLUMNW** (Unicode) 和 **LVM \_ SETCOLUMNW** (ANSI) <br/>               |



 

 





