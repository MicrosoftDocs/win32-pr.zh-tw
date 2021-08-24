---
title: 'PGM_SETBORDER 訊息 (Commctrl .h) '
description: 設定呼機控制項的目前框線大小。 您可以明確地傳送此訊息，或使用呼叫器 \_ SetBorder 宏。
ms.assetid: 073a1f9e-f05b-4203-9035-8106e87e55cd
keywords:
- PGM_SETBORDER 訊息 Windows 控制項
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
ms.openlocfilehash: 4c44433189c9d791aba1d50372176309682c1361c5b0efe31b11aaa99e9b322b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540528"
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
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





