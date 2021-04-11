---
title: 'LVM_GETSUBITEMRECT 訊息 (Commctrl .h) '
description: 針對清單視圖控制項中的子工作，取得周框矩形的相關資訊。
ms.assetid: 985876b2-6eb3-4c96-88ea-ddec67ef5b5a
keywords:
- LVM_GETSUBITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETSUBITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd1184c52d60b86e008685b87c9f5555cf801b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105491"
---
# <a name="lvm_getsubitemrect-message"></a>LVM \_ GETSUBITEMRECT 訊息

針對清單視圖控制項中的子工作，取得周框矩形的相關資訊。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetSubItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getsubitemrect) 宏 (建議的) 。 此訊息僅供使用 [**lvs) \_ 報表**](list-view-window-styles.md) 樣式的清單視圖控制項使用。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

子專案父專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標，此結構會接收子內容周框的資訊。 其成員必須根據下列成員/值關聯性進行初始化：



| 值                                                                                                                             | 意義                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**top**</dt> </dl>    | 子索引的以一為基礎的索引。<br/>                                                                                    |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**離開**</dt> </dl> | 旗標值 (查看備註) 。 表示要取得周框矩形的清單-view 子下拉式清單部分。<br/> |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

以下是可以設定的旗標值。



| 需求 | 值 |
|----------------|---------------------------------------------------------------------------------------------------------------------|
| **旗標值** | **意義**                                                                                                         |
| LVIR \_ 界限   | 傳回整個專案的周框，包括圖示和標籤。                                    |
| LVIR \_ 圖示     | 傳回圖示或小圖示的周框。                                                           |
| LVIR \_ 標籤    | 傳回整個專案的周框，包括圖示和標籤。 這與 LVIR 界限相同 \_ 。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

