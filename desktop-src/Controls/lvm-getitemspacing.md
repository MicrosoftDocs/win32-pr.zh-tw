---
title: 'LVM_GETITEMSPACING 訊息 (Commctrl .h) '
description: 決定清單視圖控制項中專案之間的間距。 您可以明確地傳送此訊息，或使用 ListView \_ GetItemSpacing 宏來傳送。
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- LVM_GETITEMSPACING message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934898"
---
# <a name="lvm_getitemspacing-message"></a>LVM \_ GETITEMSPACING 訊息

決定清單視圖控制項中專案之間的間距。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetItemSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取得其專案間距的視圖。 此參數適用 **于小型** 圖示視圖，或針對圖示視圖則為 **FALSE** 。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回專案之間的間距量。 水準間距會包含在 [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) 中，而且垂直間距會包含在 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

