---
title: 'TCM_SETPADDING 訊息 (Commctrl .h) '
description: 設定在索引標籤控制項中每個索引標籤的圖示和標籤周圍的空間 (填補) 。 您可以使用 TabCtrl SetPadding 宏明確地傳送此訊息 \_ 。
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 969ae3c7c240c38a6643682321c14e5744f2d2c2eec188004d1c3b2e6f2b3835
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876238"
---
# <a name="tcm_setpadding-message"></a>TCM \_ SETPADDING 訊息

設定在索引標籤控制項中每個索引標籤的圖示和標籤周圍的空間 (填補) 。 您可以使用 [**TabCtrl \_ SetPadding**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setpadding) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*lParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))是 **INT** 值，可指定水準填補量（以圖元為單位）。 [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))是 **INT** 值，可指定垂直填補量（以圖元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

