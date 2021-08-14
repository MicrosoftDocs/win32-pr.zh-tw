---
title: 'HDM_GETBITMAPMARGIN 訊息 (Commctrl .h) '
description: 取得標題控制項之點陣圖邊界的寬度。 您可以明確地傳送此訊息，或使用標頭 \_ GetBitmapMargin 宏。
ms.assetid: 67794ad4-3c22-4fad-a1d7-7a5d5cc6ad67
keywords:
- HDM_GETBITMAPMARGIN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_GETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 685fb96e2ecf97a33b264de7bb3a6579f0c3480b6a15fdf99929ae879f4b35c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436208"
---
# <a name="hdm_getbitmapmargin-message"></a>HDM \_ GETBITMAPMARGIN 訊息

取得標題控制項之點陣圖邊界的寬度。 您可以明確地傳送此訊息，或使用 [**標頭 \_ GetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_getbitmapmargin) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回點陣圖邊界的寬度（以圖元為單位）。 如果之前未指定點陣圖邊界，則會傳回預設值 3 \* [**GETSYSTEMMETRICS**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (SM \_ CXEDGE) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**HDM \_ SETBITMAPMARGIN**](hdm-setbitmapmargin.md)
</dt> </dl>

 

