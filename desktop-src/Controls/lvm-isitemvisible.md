---
title: 'LVM_ISITEMVISIBLE 訊息 (Commctrl .h) '
description: 指出是否可以看見清單視圖控制項中的專案。 明確地傳送此訊息，或使用 ListView \_ IsItemVisible 宏。
ms.assetid: 355be527-e2b9-46be-96a0-951d72216d92
keywords:
- LVM_ISITEMVISIBLE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_ISITEMVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 424d321b79b4a4f497942c36ca78c751cc5404cdfaf965b451eea94a8b3c8e1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958177"
---
# <a name="lvm_isitemvisible-message"></a>LVM \_ ISITEMVISIBLE 訊息

指出是否可以看見清單視圖控制項中的專案。 明確地傳送此訊息，或使用 [**ListView \_ IsItemVisible**](/windows/desktop/api/Commctrl/nf-commctrl-listview_isitemvisible) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

清單視圖控制項中專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果 **為** 可見，則傳回 TRUE，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





