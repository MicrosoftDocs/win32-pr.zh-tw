---
title: 'PGM_SETPOS 訊息 (Commctrl .h) '
description: 設定呼機控制項目前的滾動位置。 您可以明確地傳送此訊息，或使用呼叫器 \_ SetPos 宏。
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- PGM_SETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685838"
---
# <a name="pgm_setpos-message"></a>PGM \_ SETPOS 訊息

設定呼機控制項目前的滾動位置。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

**Int** 類型的值，其中包含新的捲軸位置（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





