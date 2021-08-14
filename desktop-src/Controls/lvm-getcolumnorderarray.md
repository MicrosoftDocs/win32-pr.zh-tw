---
title: 'LVM_GETCOLUMNORDERARRAY 訊息 (Commctrl .h) '
description: 取得清單視圖控制項中資料行的目前由左到右的順序。 您可以明確地傳送此訊息，或使用 ListView \_ GetColumnOrderArray 宏。
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- LVM_GETCOLUMNORDERARRAY 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea54c633c7ffc9bc580609678e8ba5f62e29429aaea6f866bb7d72b6ea326eb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411494"
---
# <a name="lvm_getcolumnorderarray-message"></a>LVM \_ GETCOLUMNORDERARRAY 訊息

取得清單視圖控制項中資料行的目前由左到右的順序。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單視圖控制項中的資料行數目。

</dd> <dt>

*lParam* 
</dt> <dd>

整數陣列的指標，這個陣列會接收清單視圖控制項中資料行的索引值。 陣列必須夠大，才能容納 *wParam* 元素。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，會傳回非零，而 *lParam* 的緩衝區會接收控制項中每個資料行的資料行索引（依其出現的順序，由左至右排列）。 否則，傳回值為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





