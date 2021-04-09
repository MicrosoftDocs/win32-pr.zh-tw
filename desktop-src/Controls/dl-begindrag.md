---
title: 'DL_BEGINDRAG (Commctrl 的通知碼) '
description: 通知拖曳清單方塊的父視窗，指出使用者已按下某個專案的滑鼠左鍵。 拖曳清單方塊會以拖曳清單訊息的形式傳送此通知碼。 如需詳細資訊，請參閱拖曳清單方塊訊息。
ms.assetid: ccf66818-e5f7-4165-8d0d-4d279944f70e
keywords:
- DL_BEGINDRAG 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DL_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2d3ee211641c5b5e02482f914145fdf2e119f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844495"
---
# <a name="dl_begindrag-notification-code"></a>DL \_ BEGINDRAG 通知碼

通知拖曳清單方塊的父視窗，指出使用者已按下某個專案的滑鼠左鍵。 拖曳清單方塊會以拖曳清單訊息的形式傳送此通知碼。 如需詳細資訊，請參閱 [拖曳清單方塊訊息](about-list-boxes.md)。


```C++
DL_BEGINDRAG

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam; 
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)結構的指標，其中包含 DL \_ BEGINDRAG 通知碼、拖曳清單方塊的控制碼，以及游標位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **TRUE** 以開始拖曳作業，或傳回 **FALSE** 以防止拖曳作業。

## <a name="remarks"></a>備註

處理此通知程式碼時，視窗程式通常會使用 [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) 函數來判斷指定之資料指標位置的清單專案。 然後，它會傳回 **TRUE** 或 **FALSE**，取決於是否應該拖曳專案。 在傳回 **TRUE** 之前，視窗程式應儲存清單專案的索引，讓應用程式知道拖曳作業完成時要移動或複製的專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





