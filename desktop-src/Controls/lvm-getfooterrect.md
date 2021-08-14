---
title: 'LVM_GETFOOTERRECT 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項頁尾的座標。 明確地傳送此訊息，或使用 ListView \_ GetFooterRect 宏。
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- LVM_GETFOOTERRECT 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39bc2c5cd724c9b5b4885b99123489e49ead52243d43388e7eb22808fb43a826
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411457"
---
# <a name="lvm_getfooterrect-message"></a>LVM \_ GETFOOTERRECT 訊息

抓取清單視圖控制項頁尾的座標。 明確地傳送此訊息，或使用 [**ListView \_ GetFooterRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用。 必須是 0。

</dd> <dt>

*lParam* \[in、out\]
</dt> <dd>

要接收座標的 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構指標。 呼叫進程負責配置此結構。 收到的座標會以用戶端座標表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功， **則傳回 TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

