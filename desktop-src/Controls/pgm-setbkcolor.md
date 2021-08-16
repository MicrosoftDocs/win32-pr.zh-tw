---
title: 'PGM_SETBKCOLOR 訊息 (Commctrl .h) '
description: 設定呼機控制項目前的背景色彩。 您可以明確地傳送此訊息，或使用呼叫器 \_ SetBkColor 宏。
ms.assetid: 720a25d7-3854-4f28-b227-bafab7b1e8c9
keywords:
- PGM_SETBKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d727bf401fae3b8c58b96fe8b5190a3ad427abb40b0478d59de087add553ddf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830179"
---
# <a name="pgm_setbkcolor-message"></a>PGM \_ SETBKCOLOR 訊息

設定呼機控制項目前的背景色彩。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setbkcolor) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

**COLORREF** 值，其中包含分頁控制項的新背景色彩。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含先前背景色彩的 **COLORREF** 值。

## <a name="remarks"></a>備註

根據預設，分頁控制項會使用系統按鈕的臉部色彩做為背景色彩。 這種色彩可透過呼叫 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 和 color BTNFACE 來抓取 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

