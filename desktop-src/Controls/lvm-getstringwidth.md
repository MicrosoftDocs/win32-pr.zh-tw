---
title: 'LVM_GETSTRINGWIDTH 訊息 (Commctrl .h) '
description: 使用指定的清單視圖控制項目前字型，判斷指定之字串的寬度。 您可以明確地傳送此訊息，或使用 ListView \_ GetStringWidth 宏來傳送。
ms.assetid: ffe97640-d4b6-45ae-be5d-71fed69c2026
keywords:
- LVM_GETSTRINGWIDTH 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETSTRINGWIDTH
- LVM_GETSTRINGWIDTHA
- LVM_GETSTRINGWIDTHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9024cab94f59e543351e06d49ec058435ae369b6b746b1dc3fb2cd0472e3d57e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019306"
---
# <a name="lvm_getstringwidth-message"></a>LVM \_ GETSTRINGWIDTH 訊息

使用指定的清單視圖控制項目前字型，判斷指定之字串的寬度。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetStringWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getstringwidth) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

以 null 結束的字串指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回字串寬度，否則傳回零。

## <a name="remarks"></a>備註

LVM \_ GETSTRINGWIDTH 訊息會傳回指定字串的確切寬度（以圖元為單位）。 如果您使用傳回的字串寬度做為 [**LVM \_ SETCOLUMNWIDTH**](lvm-setcolumnwidth.md) 訊息中的資料行寬度，則會截斷字串。 若要在不截斷的情況下，取得可包含字串的資料行寬度，您必須在傳回的字串寬度加上填補。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **LVM \_GETSTRINGWIDTHW** (Unicode) 和 **LVM \_ GETSTRINGWIDTHA** (ANSI) <br/>     |



 

 





