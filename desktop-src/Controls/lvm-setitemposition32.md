---
title: 'LVM_SETITEMPOSITION32 訊息 (Commctrl .h) '
description: 將專案移至清單視圖控制項中的指定位置 (必須是圖示或小圖示視圖) 。
ms.assetid: 77db5fd0-bbc3-47ad-95ef-61ef4ac022bc
keywords:
- LVM_SETITEMPOSITION32 message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETITEMPOSITION32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 450963e4adf5ea2b0644f8d155145ba577efab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025154"
---
# <a name="lvm_setitemposition32-message"></a>LVM \_ SETITEMPOSITION32 訊息

將專案移至清單視圖控制項中的指定位置 (必須是圖示或小圖示視圖) 。 這則訊息與 [**LVM \_ SETITEMPOSITION**](lvm-setitemposition.md) 訊息不同，因為它使用32位的座標。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetItemPosition32**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemposition32) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要設定其位置之清單視圖專案的索引。

</dd> <dt>

*lParam* 
</dt> <dd>

[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，其中包含專案的新位置，以清單視圖座標為單位。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

