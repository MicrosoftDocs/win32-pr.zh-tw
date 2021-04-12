---
title: 'LVM_GETVIEWRECT 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項中所有專案的周框。 清單視圖必須在圖示或小型圖示視圖中。 您可以明確地傳送此訊息，或使用 ListView \_ GetViewRect 宏來傳送。
ms.assetid: 69b96f86-8b7e-42c1-ad73-f9b2732ab9f9
keywords:
- LVM_GETVIEWRECT message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETVIEWRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d4c4fdf0e8466d3fb0b2ad164241c3f6a541570
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025374"
---
# <a name="lvm_getviewrect-message"></a>LVM \_ GETVIEWRECT 訊息

抓取清單視圖控制項中所有專案的周框。 清單視圖必須在圖示或小型圖示視圖中。 您可以明確地傳送此訊息，或使用 [**ListView \_ GetViewRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getviewrect) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

接收周框 [**的矩形結構指標**](/previous-versions//dd162897(v=vs.85)) 。 所有座標都是相對於清單視圖控制項的可見區域。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

