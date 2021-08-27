---
title: 'LVM_SETCALLBACKMASK 訊息 (Commctrl .h) '
description: 變更清單視圖控制項的回呼遮罩。 您可以明確地傳送此訊息，或使用 ListView \_ SetCallbackMask 宏來傳送。
ms.assetid: d7828bab-9897-408c-99ca-fad42b431be8
keywords:
- LVM_SETCALLBACKMASK 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79e33b106eb0c59f83e40b9f170dd017fcdda412072ed51a26572fcf368f5215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088848"
---
# <a name="lvm_setcallbackmask-message"></a>LVM \_ SETCALLBACKMASK 訊息

變更清單視圖控制項的回呼遮罩。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcallbackmask) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

回呼遮罩的值。 遮罩的位表示應用程式儲存目前狀態資料的專案狀態或影像。 這個值可以是下列常數的任意組合：



| 值                                                                                                                                                                           | 意義                                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span id="LVIS_CUT"></span><span id="lvis_cut"></span><dl> <dt>**LVIS \_ 剪下**</dt> </dl>                                  | ：項目已標記為進行剪貼作業。<br/>                                       |
| <span id="LVIS_DROPHILITED"></span><span id="lvis_drophilited"></span><dl> <dt>**LVIS \_ DROPHILITED**</dt> </dl>          | ：項目會隨著拖放目標而反白顯示。<br/>                                      |
| <span id="LVIS_FOCUSED"></span><span id="lvis_focused"></span><dl> <dt>**LVIS \_ 焦點**</dt> </dl>                      | ：項目具有焦點。<br/>                                                                 |
| <span id="LVIS_SELECTED"></span><span id="lvis_selected"></span><dl> <dt>**LVIS 已 \_ 選取**</dt> </dl>                   | 這個項目已選取。 <br/>                                                                  |
| <span id="LVIS_OVERLAYMASK"></span><span id="lvis_overlaymask"></span><dl> <dt>**LVIS \_ OVERLAYMASK**</dt> </dl>          | 應用程式會儲存每個專案之目前覆迭影像的影像清單索引。<br/> |
| <span id="LVIS_STATEIMAGEMASK"></span><span id="lvis_stateimagemask"></span><dl> <dt>**LVIS \_ STATEIMAGEMASK**</dt> </dl> | 應用程式會儲存每個專案之目前狀態影像的影像清單索引。 <br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

清單視圖控制項的 *回呼遮罩* 是一組位旗標，用來指定應用程式（而非控制項）儲存目前資料的專案狀態。 回呼遮罩適用於所有控制項的項目，與套用至特定項目的回呼項目指定不同。 回呼遮罩預設為零，表示清單視圖控制項會儲存所有專案狀態資訊。 建立清單視圖控制項並初始化其專案之後，您可以傳送 **LVM \_ SETCALLBACKMASK** 訊息來變更回呼遮罩。 若要取得目前的回呼遮罩，請傳送 [**LVM \_ GETCALLBACKMASK**](lvm-getcallbackmask.md) 訊息。

如需覆迭影像和狀態影像的詳細資訊，請參閱 [新增 List-View 的影像清單](using-list-view-controls.md)。

如需清單視圖回呼的詳細資訊，請參閱 [回呼專案和回呼遮罩](list-view-controls-overview.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LVN \_ GETDISPINFO**](lvn-getdispinfo.md)
</dt> </dl>

 

 





