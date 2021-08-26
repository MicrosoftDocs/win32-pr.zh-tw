---
title: 'PGM_SETPOS 訊息 (Commctrl .h) '
description: 設定呼機控制項目前的滾動位置。 您可以明確地傳送此訊息，或使用呼叫器 \_ SetPos 宏。
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- PGM_SETPOS 訊息 Windows 控制項
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
ms.openlocfilehash: a7a056d55d0ec70b3ff3068580c1e9923b363efa15e9ab26bf8aa67f476cc147
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046827"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





