---
title: 'HDM_SETBITMAPMARGIN 訊息 (Commctrl .h) '
description: 在現有的標題控制項中，設定點陣圖的邊界寬度（以圖元為單位）。 您可以明確地傳送此訊息，或使用標頭 \_ SetBitmapMargin 宏。
ms.assetid: 5ac04701-18c8-42d4-9850-fe6eb813672c
keywords:
- HDM_SETBITMAPMARGIN 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- HDM_SETBITMAPMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2e7c24ea52edc0001cea9f4d7184957c2cfbf50f15769df964351df91e5813
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435948"
---
# <a name="hdm_setbitmapmargin-message"></a>HDM \_ SETBITMAPMARGIN 訊息

在現有的標題控制項中，設定點陣圖的邊界寬度（以圖元為單位）。 您可以明確地傳送此訊息，或使用 [**標頭 \_ SetBitmapMargin**](/windows/desktop/api/Commctrl/nf-commctrl-header_setbitmapmargin) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

在現有的標題控制項內圍住點陣圖之邊界的寬度（以圖元為單位）。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回點陣圖邊界的寬度（以圖元為單位）。 如果之前未指定點陣圖邊界，則會傳回預設值 3 \* [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) (*SM \_ CXEDGE*) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**HDM \_ GETBITMAPMARGIN**](hdm-getbitmapmargin.md)
</dt> </dl>

 

