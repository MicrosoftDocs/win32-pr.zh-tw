---
title: 'LVM_CREATEDRAGIMAGE 訊息 (Commctrl .h) '
description: 為指定的專案建立拖曳影像清單。 您可以明確地傳送此訊息，或使用 ListView \_ CreateDragImage 宏來傳送。
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- LVM_CREATEDRAGIMAGE message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093855"
---
# <a name="lvm_createdragimage-message"></a>LVM \_ CREATEDRAGIMAGE 訊息

為指定的專案建立拖曳影像清單。 您可以明確地傳送此訊息，或使用 [**ListView \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

項目的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，該結構會接收影像左上角的初始位置（以視圖座標表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回拖曳影像清單的控制碼，否則傳回 **Null** 。

## <a name="remarks"></a>備註

當不再需要時，您的應用程式會負責終結影像清單。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

