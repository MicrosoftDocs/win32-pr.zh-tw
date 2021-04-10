---
title: 'LVM_ARRANGE 訊息 (Commctrl .h) '
description: 在圖示視圖中排列專案。 您可以明確地傳送此訊息，或使用 ListView \_ 排列宏來傳送。
ms.assetid: f7dbcdd2-3cc9-4bae-827e-8bac3b49486c
keywords:
- LVM_ARRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_ARRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a1b6a081cf963a649329951358ea4c972f200f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093859"
---
# <a name="lvm_arrange-message"></a>LVM \_ 排列訊息

在圖示視圖中排列專案。 您可以明確地傳送此訊息，或使用 [**ListView \_ 排列**](/windows/desktop/api/Commctrl/nf-commctrl-listview_arrange) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

下列其中一個值會指定對齊：



| 值                                                                                                                                                            | 意義                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span id="LVA_ALIGNLEFT"></span><span id="lva_alignleft"></span><dl> <dt>**LVA \_ ALIGNLEFT**</dt> </dl>    | 未實作。 請改為套用 [**lvs) \_ ALIGNLEFT**](list-view-window-styles.md) 樣式。<br/> |
| <span id="LVA_ALIGNTOP"></span><span id="lva_aligntop"></span><dl> <dt>**LVA \_ ALIGNTOP**</dt> </dl>       | 未實作。 請改為套用 [**lvs) \_ ALIGNTOP**](list-view-window-styles.md) 樣式。<br/>   |
| <span id="LVA_DEFAULT"></span><span id="lva_default"></span><dl> <dt>**LVA \_ 預設值**</dt> </dl>          | 根據清單視圖控制項的目前對齊樣式來對齊專案 (預設值) 。<br/>           |
| <span id="LVA_SNAPTOGRID"></span><span id="lva_snaptogrid"></span><dl> <dt>**LVA \_ 格線**</dt> </dl> | 將所有圖示貼齊最接近的方格位置。<br/>                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 **TRUE** ;否則 **為 FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





