---
title: 'LVM_SETITEMSTATE 訊息 (Commctrl .h) '
description: 變更清單視圖控制項中專案的狀態。 您可以明確地傳送此訊息，或使用 ListView \_ SetItemState 宏來傳送。
ms.assetid: aecd14dd-cfd0-4c7c-bddc-f65022de68c9
keywords:
- LVM_SETITEMSTATE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92b7375ad7edb32459fe6029081ec0a872d3673c90003e34ca21cd795d3a79ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217413"
---
# <a name="lvm_setitemstate-message"></a>LVM \_ SETITEMSTATE 訊息

變更清單視圖控制項中專案的狀態。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemstate) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單視圖專案的索引。 如果此參數為-1，則狀態變更會套用至所有專案。

</dd> <dt>

*lParam* 
</dt> <dd>

[**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema)結構的指標。 **StateMask** 成員會指定要變更的狀態位，而且 **狀態** 成員會包含這些位的新值。 其他成員則會被忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果您明確傳送此訊息，則會在成功時傳回 **TRUE** ，否則會傳回 **FALSE** 。

## <a name="remarks"></a>備註

專案的狀態值包含一組位旗標，指出專案的狀態。 狀態值也可以包含表示專案狀態影像和重迭影像的影像清單索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





