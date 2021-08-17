---
title: 'LVM_GETITEMSTATE 訊息 (Commctrl .h) '
description: 抓取清單視圖專案的狀態。 您可以明確地傳送此訊息，或使用 ListView \_ GetItemState 宏來傳送。
ms.assetid: 862960ed-a64a-4d66-b384-9228932eae6f
keywords:
- LVM_GETITEMSTATE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4737be14f3e975f87a6cbea460ef53dd40ecbb7b6a2d06c39a247dbe8aa0a14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958297"
---
# <a name="lvm_getitemstate-message"></a>LVM \_ GETITEMSTATE 訊息

抓取清單視圖專案的狀態。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetItemState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemstate) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

清單視圖專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

要取出的狀態資訊。 這個參數可以是下列值的組合：



| 值                                                                                                                                                                           | 意義                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ 剪下**</dt> </dl>                                  | ：項目已標記為進行剪貼作業。<br/>                                                                                                         |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | ：項目會隨著拖放目標而反白顯示。<br/>                                                                                                        |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ 焦點**</dt> </dl>                      | 專案具有焦點，因此會以標準焦點矩形括住。 雖然可以選取一個以上的專案，但只有一個專案可以有焦點。<br/> |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS 已 \_ 選取**</dt> </dl>                   | 這個項目已選取。 選取專案的外觀取決於它是否具有焦點，也會顯示用於選取的系統色彩。<br/>             |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | 使用此遮罩來抓取專案的重迭影像索引。<br/>                                                                                                 |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | 使用此遮罩來取得專案的狀態影像索引。<br/>                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回指定之專案的目前狀態。 傳回值中唯一有效的位是對應至 *lParam* 參數中所設定之位的有效位。

## <a name="remarks"></a>備註

專案的狀態資訊包含一組位旗標，以及表示專案狀態影像和重迭影像的影像清單索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LVM \_ SETITEMSTATE**](lvm-setitemstate.md)
</dt> </dl>

 

 





