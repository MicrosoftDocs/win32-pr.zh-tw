---
title: 'LVM_GETFOOTERITEMRECT 訊息 (Commctrl .h) '
description: 取得清單視圖控制項中指定專案之頁尾的座標。 明確地傳送此訊息，或使用 ListView \_ GetFooterItemRect 宏。
ms.assetid: 4a6055d3-1cc1-4c3d-a5f6-006617ff3bce
keywords:
- LVM_GETFOOTERITEMRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETFOOTERITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142cb92806fa1d58faa0414c10c41bd2815d5b6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187271"
---
# <a name="lvm_getfooteritemrect-message"></a>LVM \_ GETFOOTERITEMRECT 訊息

取得清單視圖控制項中指定專案之頁尾的座標。 明確地傳送此訊息，或使用 [**ListView \_ GetFooterItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooteritemrect) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* \[在\]
</dt> <dd>

清單視圖控制項中專案的索引。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

要接收座標的 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構指標。 呼叫應用程式負責配置此結構。 收到的座標會以用戶端座標表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

