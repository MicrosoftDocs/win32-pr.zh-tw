---
title: 'LVM_SETTEXTCOLOR 訊息 (Commctrl .h) '
description: 設定清單視圖控制項的文字色彩。 您可以明確地傳送此訊息，或使用 ListView \_ SetTextColor 宏來傳送。
ms.assetid: ff90c18b-0cd7-4331-bcd8-61044e891d1f
keywords:
- LVM_SETTEXTCOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64b30c965bd523cd5638c894b47fc4785ffbdd09
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094304"
---
# <a name="lvm_settextcolor-message"></a>LVM \_ SETTEXTCOLOR 訊息

設定清單視圖控制項的文字色彩。 您可以明確地傳送此訊息，或使用 [**ListView \_ SetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextcolor) 宏來傳送。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

指定新文字色彩的 [**COLORREF**](/windows/desktop/gdi/colorref) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

