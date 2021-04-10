---
title: 'LVM_GETITEMRECT 訊息 (Commctrl .h) '
description: 抓取目前視圖中所有或部分專案的周框。 您可以明確地傳送此訊息，或使用 ListView \_ GetItemRect 宏來傳送。
ms.assetid: 7ce74b65-3360-42b4-9889-d90aefe2d284
keywords:
- LVM_GETITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0915c9afc16f13ac8f36a639524fb5af6e8082
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025378"
---
# <a name="lvm_getitemrect-message"></a>LVM \_ GETITEMRECT 訊息

抓取目前視圖中所有或部分專案的周框。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemrect) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

清單視圖專案的索引。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

接收周框 [**的矩形結構指標**](/previous-versions//dd162897(v=vs.85)) 。 傳送訊息時，會使用此結構的 **左側** 成員來指定清單視圖專案的部分，以從中取出周框。 它必須設定為下列其中一個值：



| 值                                                                                                                                                                     | 意義                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**LVIR \_ 界限**</dt> </dl>                   | 傳回整個專案的周框，包括圖示和標籤。<br/>                     |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**LVIR \_ 圖示**</dt> </dl>                         | 傳回圖示或小圖示的周框。<br/>                                            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**LVIR \_ 標籤**</dt> </dl>                      | 傳回專案文字的周框。<br/>                                                     |
| <span id="LVIR_SELECTBOUNDS"></span><span id="lvir_selectbounds"></span><dl> <dt>**LVIR \_ SELECTBOUNDS**</dt> </dl> | 傳回 LVIR \_ 圖示和 LVIR \_ 標籤矩形的聯集，但在報表檢視中排除資料行。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

