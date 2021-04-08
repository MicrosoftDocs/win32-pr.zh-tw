---
title: 'LVM_SETSELECTIONMARK 訊息 (Commctrl .h) '
description: 設定清單視圖控制項中的選取專案標記。 您可以明確地傳送此訊息，或使用 ListView \_ SetSelectionMark 宏。
ms.assetid: 3218f1b3-b934-4083-aaaa-e10ef1dbb6bd
keywords:
- LVM_SETSELECTIONMARK message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETSELECTIONMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efc01068f22585061cae5a6f2c5c0c841810f52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685516"
---
# <a name="lvm_setselectionmark-message"></a>LVM \_ SETSELECTIONMARK 訊息

設定清單視圖控制項中的選取專案標記。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetSelectionMark**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setselectionmark) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

新選取標記的以零為起始的索引。 如果設定為-1，則會移除選取標記。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回先前的選取專案標記，如果沒有上一個選取專案標記，則為-1。

## <a name="remarks"></a>備註

*選取標記* 是從其開始多重選取專案的專案索引。 此訊息不會影響專案的選取狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LVM \_ GETSELECTIONMARK**](lvm-getselectionmark.md)
</dt> </dl>

 

 





