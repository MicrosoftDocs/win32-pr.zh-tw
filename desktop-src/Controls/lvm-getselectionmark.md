---
title: 'LVM_GETSELECTIONMARK 訊息 (Commctrl .h) '
description: 從清單視圖控制項抓取選取標記。 您可以明確地傳送此訊息，或使用 ListView \_ GetSelectionMark 宏。
ms.assetid: 21daf7d7-1217-4608-93f9-c390546f1591
keywords:
- LVM_GETSELECTIONMARK message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 076aff15ff69c4b442c74022ed5a7c02b92a8c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965749"
---
# <a name="lvm_getselectionmark-message"></a>LVM \_ GETSELECTIONMARK 訊息

從清單視圖控制項抓取選取標記。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectionmark) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回以零為基底的選取標記; 如果沒有選取專案標記，則為-1。

## <a name="remarks"></a>備註

*選取標記* 是從其開始多重選取專案的專案索引。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LVM \_ SETSELECTIONMARK**](lvm-setselectionmark.md)
</dt> </dl>

 

 





