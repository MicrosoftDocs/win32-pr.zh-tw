---
title: 'DL_DROPPED (Commctrl 的通知碼) '
description: 透過放開滑鼠左鍵，表示使用者已完成拖曳操作。 拖曳清單方塊會將此通知碼以拖曳清單訊息的形式傳送至其父視窗。 如需詳細資訊，請參閱拖曳清單方塊訊息。
ms.assetid: 81b9b424-2735-407d-bac9-f03ea2f48b4e
keywords:
- DL_DROPPED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- DL_DROPPED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b2480360ea38a00c4dd8efe6eb84eed8999890
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844496"
---
# <a name="dl_dropped-notification-code"></a>DL 已卸載 \_ 通知碼

透過放開滑鼠左鍵，表示使用者已完成拖曳操作。 拖曳清單方塊會將此通知碼以拖曳清單訊息的形式傳送至其父視窗。 如需詳細資訊，請參閱 [拖曳清單方塊訊息](about-list-boxes.md)。


```C++
DL_DROPPED

    pDragInfo = (LPARAM)(LPDRAGLISTINFO) lParam;
```



## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**DRAGLISTINFO**](/windows/win32/api/commctrl/ns-commctrl-draglistinfo)結構的指標，其中包含 DL 卸載的 \_ 通知碼、拖曳清單方塊的控制碼，以及游標位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

通常會藉由將拖曳的專案插入至游標下專案前面的清單來處理此通知碼。 若要在游標位置取出專案的索引，請使用 [**LBItemFromPt**](/windows/desktop/api/Commctrl/nf-commctrl-lbitemfrompt) 函數。 請注意， \_ 即使資料指標不在清單專案上，仍會傳送 DL 捨棄的通知碼。 在此情況下， **LBItemFromPt** 會傳回-1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





