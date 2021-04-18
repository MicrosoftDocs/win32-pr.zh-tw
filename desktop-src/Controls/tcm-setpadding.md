---
title: 'TCM_SETPADDING 訊息 (Commctrl .h) '
description: 設定在索引標籤控制項中每個索引標籤的圖示和標籤周圍的空間 (填補) 。 您可以使用 TabCtrl SetPadding 宏明確地傳送此訊息 \_ 。
ms.assetid: c7f84c0d-8bf4-429a-b403-a0019575e72e
keywords:
- TCM_SETPADDING message Windows 控制項
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
ms.openlocfilehash: 353cde946944bda7dc8d285f863d976e29353996
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965693"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

