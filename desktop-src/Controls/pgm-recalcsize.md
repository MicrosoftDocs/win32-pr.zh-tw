---
title: 'PGM_RECALCSIZE 訊息 (Commctrl .h) '
description: 強制呼機控制項重新計算包含視窗的大小。 傳送此訊息將會產生 PGN \_ CALCSIZE 通知。 您可以明確地傳送此訊息，或使用呼叫器 \_ RecalcSize 宏。
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- PGM_RECALCSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465037"
---
# <a name="pgm_recalcsize-message"></a>PGM \_ RECALCSIZE 訊息

強制呼機控制項重新計算包含視窗的大小。 傳送此訊息將會產生 [PGN \_ CALCSIZE](pgn-calcsize.md) 通知。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ RecalcSize**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





