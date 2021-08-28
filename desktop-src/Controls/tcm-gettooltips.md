---
title: 'TCM_GETTOOLTIPS 訊息 (Commctrl .h) '
description: 抓取與索引標籤控制項相關聯的工具提示控制項控點。 您可以使用 TabCtrl GetToolTips 宏明確地傳送此訊息 \_ 。
ms.assetid: d7dcca4f-8629-4eeb-844f-b3171438f528
keywords:
- TCM_GETTOOLTIPS 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- TCM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb68710c13c8b6b236782b133caa5b6f3609fef931e3b1e395b9944e9ab9a651
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166931"
---
# <a name="tcm_gettooltips-message"></a>TCM \_ GETTOOLTIPS 訊息

抓取與索引標籤控制項相關聯的工具提示控制項控點。 您可以使用 [**TabCtrl \_ GetToolTips**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_gettooltips) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回工具提示控制項的控制碼，否則傳回 **Null** 。

## <a name="remarks"></a>備註

如果工具提示控制項有 [**TCS \_ 工具提示**](tab-control-styles.md) 樣式，則會建立工具提示控制項。 您也可以使用 [**TCM \_ SETTOOLTIPS**](tcm-settooltips.md) 訊息，將工具提示控制項指派給索引標籤控制項。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





