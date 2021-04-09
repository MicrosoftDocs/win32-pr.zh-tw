---
title: 'PGM_SETBORDER 訊息 (Commctrl .h) '
description: 設定呼機控制項的目前框線大小。 您可以明確地傳送此訊息，或使用呼叫器 \_ SetBorder 宏。
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- PGM_SETBORDER message Windows 控制項
topic_type:
- apiref
api_name:
- PGM_SETBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a987246a56da213098ba8632044af97ae51462df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024992"
---
# <a name="pgm_setborder-message"></a>PGM \_ SETBORDER 訊息

設定呼機控制項的目前框線大小。 您可以明確地傳送此訊息，或使用 [**呼叫器 \_ SetBorder**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setborder) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

框線的新大小（以圖元為單位）。 此值不應大於呼機按鈕或小於零。 如果 *lParam* 太大，框線將會繪製成與按鈕相同的大小。 如果 *lParam* 為負數，則框線大小將設定為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含先前框線大小的 INT 值（以圖元為單位）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





