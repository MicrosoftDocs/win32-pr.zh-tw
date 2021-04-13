---
title: 'DL_DRAGGING (Commctrl 的通知碼) '
description: 指出使用者在拖曳專案時移動滑鼠的信號。
ms.assetid: 87fc4c24-8e88-4e3c-8f54-ecc7f80de5d7
keywords:
- DL_DRAGGING 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DL_DRAGGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5c9f3f6cec3ef95745eed88ec0208dff581ada
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509496"
---
# <a name="dl_dragging-notification-code"></a>DL \_ 拖曳通知碼

指出使用者在拖曳專案時移動滑鼠的信號。 \_即使滑鼠未移動，也會在拖曳期間定期傳送 DL 拖曳。 拖曳清單方塊會將此通知碼以拖曳清單訊息的形式傳送至其父視窗。 如需詳細資訊，請參閱 [拖曳清單方塊訊息](about-list-boxes.md)。


```C++
DL_DRAGGING

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

拖曳清單方塊的控制項識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>

[**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)結構的指標，其中包含 DL \_ 拖曳通知碼、拖曳清單方塊的控制碼，以及游標位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值決定拖曳清單應設定的滑鼠游標類型;它可以是 DL \_ STOPCURSOR、dl \_ COPYCURSOR 或 dl \_ MOVECURSOR 值。 如果傳回任何其他值，則不會變更資料指標。

## <a name="remarks"></a>備註

視窗程式通常會藉 \_ 由判斷游標下的專案，然後繪製插入圖示，來處理 DL 拖曳通知程式碼。 若要取得資料指標下的專案，請使用 [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt)函式，針對 *BAutoScroll* 參數指定 **TRUE** 。 如果游標位於其工作區的上方或下方，此選項會讓拖曳清單方塊定期滾動。 若要繪製插入圖示，請使用 [**DrawInsert**](/windows/desktop/api/Commctrl/nf-commctrl-drawinsert) 函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





