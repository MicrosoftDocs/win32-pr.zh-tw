---
title: 'LVM_GETFOOTERRECT 訊息 (Commctrl .h) '
description: 抓取清單視圖控制項頁尾的座標。 明確地傳送此訊息，或使用 ListView \_ GetFooterRect 宏。
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- LVM_GETFOOTERRECT message Windows 控制項
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
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093843"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

