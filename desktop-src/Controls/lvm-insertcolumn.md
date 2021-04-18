---
title: 'LVM_INSERTCOLUMN 訊息 (Commctrl .h) '
description: 在清單視圖控制項中插入新的資料行。 您可以明確地傳送此訊息，或使用 ListView \_ InsertColumn 宏來傳送。
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- LVM_INSERTCOLUMN message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509155"
---
# <a name="lvm_insertcolumn-message"></a>LVM \_ INSERTCOLUMN 訊息

在清單視圖控制項中插入新的資料行。 您可以明確地傳送此訊息，或使用 [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

新資料行的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna)結構的指標，其中包含新資料行的屬性。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回新資料行的索引，否則傳回-1。

## <a name="remarks"></a>備註

只有在報表 (詳細資料) 視圖中，才會顯示資料行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





