---
title: 'LVM_DELETEALLITEMS 訊息 (Commctrl .h) '
description: 移除清單視圖控制項中的所有專案。 您可以明確地傳送此訊息，或使用 ListView \_ DeleteAllItems 宏來傳送。
ms.assetid: 816bf565-79e9-4f5d-b5b4-5cdecce8a61c
keywords:
- LVM_DELETEALLITEMS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_DELETEALLITEMS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c81d2911caee047b63c4a637b6996bc90096e56d337f068beb73fe0fb42b4579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958407"
---
# <a name="lvm_deleteallitems-message"></a>LVM \_ DELETEALLITEMS 訊息

移除清單視圖控制項中的所有專案。 您可以明確地傳送此訊息，或使用 [**ListView \_ DeleteAllItems**](/windows/desktop/api/Commctrl/nf-commctrl-listview_deleteallitems) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

當清單視圖控制項收到 **LVM \_ DELETEALLITEMS** 訊息時，它會將 [**LVN \_ DELETEALLITEMS**](lvn-deleteallitems.md) 通知程式碼傳送至其父視窗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





