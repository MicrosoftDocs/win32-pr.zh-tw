---
title: 'LVM_SETCOLUMNORDERARRAY 訊息 (Commctrl .h) '
description: 在清單視圖控制項中設定資料行的由左到右的順序。 您可以明確地傳送此訊息，或使用 ListView \_ SetColumnOrderArray 宏。
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- LVM_SETCOLUMNORDERARRAY 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9931a7d2c12da02f928c21727292d7d1ce4a430790660afb99ede4bf717c38c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077298"
---
# <a name="lvm_setcolumnorderarray-message"></a>LVM \_ SETCOLUMNORDERARRAY 訊息

在清單視圖控制項中設定資料行的由左到右的順序。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

緩衝區的大小（以元素為 *lParam*）。

</dd> <dt>

*lParam* 
</dt> <dd>

陣列的指標，這個陣列會指定資料行的顯示順序（從左至右）。 例如，如果陣列的內容是 {2,0,1} ，控制項會依序顯示資料行2、資料行0和資料行1。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





