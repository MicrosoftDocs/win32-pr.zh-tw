---
title: 'PGM_GETBKCOLOR 訊息 (Commctrl .h) '
description: 抓取呼機控制項目前的背景色彩。 您可以明確地傳送此訊息，或使用呼叫器 \_ GetBkColor 宏。
ms.assetid: c39ad721-fe39-44e9-8305-67444acc5d65
keywords:
- PGM_GETBKCOLOR 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- PGM_GETBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff3ee3a4be09a948654d337a47eecdd2a7b15d16b0602016aa99500cd1c3728c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985938"
---
# <a name="pgm_getbkcolor-message"></a>PGM \_ GETBKCOLOR 訊息

抓取呼機控制項目前的背景色彩。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbkcolor) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **COLORREF** 值，其中包含目前的背景色彩。

## <a name="remarks"></a>備註

根據預設，分頁控制項會使用系統按鈕的臉部色彩做為背景色彩。 這種色彩可透過呼叫 [**GetSysColorBrush**](/windows/desktop/api/winuser/nf-winuser-getsyscolorbrush) 和 color BTNFACE 來抓取 \_ 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

