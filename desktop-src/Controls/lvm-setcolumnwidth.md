---
title: 'LVM_SETCOLUMNWIDTH 訊息 (Commctrl .h) '
description: 變更報表檢視模式中的資料行寬度，或在清單視圖模式中變更所有資料行的寬度。 您可以明確地傳送此訊息，或使用 ListView \_ SetColumnWidth 宏。
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- LVM_SETCOLUMNWIDTH 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a127706d6a47444ee59f1434478aadb5170f9ac7a919dca6fd6151de33486d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077288"
---
# <a name="lvm_setcolumnwidth-message"></a>LVM \_ SETCOLUMNWIDTH 訊息

變更報表檢視模式中的資料行寬度，或在清單視圖模式中變更所有資料行的寬度。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

有效資料行以零為基底的索引。 若為清單視圖模式，此參數必須設定為零。

</dd> <dt>

*lParam* 
</dt> <dd>

資料行的新寬度（以圖元為單位）。 針對報表檢視模式，支援下列特殊值：



| 值                                                                                                                                                                                           | 意義                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <dt>**LVSCW \_ AUTOSIZE**</dt> </dl>                                | 自動調整資料行的大小。<br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <dt>**LVSCW \_ AUTOSIZE \_ USEHEADER**</dt> </dl> | 自動調整資料行大小以符合標頭文字。 如果您使用此值與最後一個資料行，它的寬度會設定為填滿清單視圖控制項的剩餘寬度。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

假設您有一個寬度為500圖元的2個數據行清單視圖控制項。 如果資料行零的寬度設定為200圖元，且您使用 *wParam* = 1 和 *lParam* = LVSCW AUTOSIZE USEHEADER 來傳送此訊息， \_ \_ 則第二個 (和最後一個) 資料行將會是300圖元寬。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





