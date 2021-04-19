---
title: 'PGM_GETBORDER 訊息 (Commctrl .h) '
description: 抓取呼機控制項目前的框線大小。 您可以明確地傳送此訊息，或使用呼叫器 \_ GetBorder 宏。
ms.assetid: 5d2f49ad-d940-4a0b-b5a0-05d742151b1c
keywords:
- PGM_GETBORDER message Windows 控制項
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
ms.openlocfilehash: be510af44c9cf53000420531843a79e9856c40dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001311"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PGM \_ SETBORDER**](pgm-setborder.md)
</dt> </dl>

 

 





