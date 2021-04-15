---
title: 'LVM_GETITEMINDEXRECT 訊息 (Commctrl .h) '
description: 在清單視圖控制項的目前視圖中，抓取所有或部分子部分的周框。 明確地傳送此訊息，或使用 ListView \_ GetItemIndexRect 宏。
ms.assetid: 17704d24-c029-4d41-b198-04d1e78698e0
keywords:
- LVM_GETITEMINDEXRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETITEMINDEXRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ccd114713326c4796ca69f56fc2c38daf145db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466512"
---
# <a name="lvm_getitemindexrect-message"></a>LVM \_ GETITEMINDEXRECT 訊息

在清單視圖控制項的目前視圖中，抓取所有或部分子部分的周框。 明確地傳送此訊息，或使用 [**ListView \_ GetItemIndexRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemindexrect) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

子專案父專案的 [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) 結構指標。 呼叫進程負責配置此結構並設定其成員。 *wParam* 不得為 **Null**。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

要接收座標的 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構指標。 呼叫進程負責配置此結構。 *lParam* 不得為 **Null**。 將 **最上層** 成員設為子工作的索引。 將 **左邊** 的成員設定為下列其中一個值，表示要抓取周框的子部分。



| 值                                                                                                                                                   | 意義                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="LVIR_BOUNDS"></span><span id="lvir_bounds"></span><dl> <dt>**LVIR \_ 界限**</dt> </dl> | 傳回整個子工作的周框，包括圖示和標籤。<br/> |
| <span id="LVIR_ICON"></span><span id="lvir_icon"></span><dl> <dt>**LVIR \_ 圖示**</dt> </dl>       | 傳回子工作圖示或小圖示的周框。<br/>            |
| <span id="LVIR_LABEL"></span><span id="lvir_label"></span><dl> <dt>**LVIR \_ 標籤**</dt> </dl>    | 傳回子文字的周框。<br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

