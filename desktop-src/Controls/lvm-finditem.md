---
title: 'LVM_FINDITEM 訊息 (Commctrl .h) '
description: 搜尋具有指定特性的清單視圖專案。 您可以明確地傳送此訊息，或使用 ListView \_ FindItem 宏來傳送。
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- LVM_FINDITEM message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464288"
---
# <a name="lvm_finditem-message"></a>LVM \_ FINDITEM 訊息

搜尋具有指定特性的清單視圖專案。 您可以明確地傳送此訊息，或使用 [**ListView \_ FindItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要開始搜尋的專案索引，或-1 會從頭開始。 從搜尋中排除指定的專案。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa)結構的指標，其中包含要搜尋之內容的相關資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回專案的索引，否則傳回-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_FINDITEMW** (Unicode) 和 **LVM \_ FINDITEMA** (ANSI) <br/>                 |



 

 





