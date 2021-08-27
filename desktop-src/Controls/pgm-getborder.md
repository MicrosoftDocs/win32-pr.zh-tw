---
title: 'PGM_GETBORDER 訊息 (Commctrl .h) '
description: 抓取呼機控制項目前的框線大小。 您可以明確地傳送此訊息，或使用呼叫器 \_ GetBorder 宏。
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- PGM_GETBORDER 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PGM_GETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148b3d840548116d3082e27b5a760650c5802bdb2c6dbc1fc7c94f1df3a3d5b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046858"
---
# <a name="pgm_getborder-message"></a>PGM \_ GETBORDER 訊息

抓取呼機控制項目前的框線大小。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getborder) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含目前框線大小的 INT 值（以圖元為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PGM \_ SETBORDER**](pgm-setborder.md)
</dt> </dl>

 

 





