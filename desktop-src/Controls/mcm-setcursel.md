---
title: 'MCM_SETCURSEL 訊息 (Commctrl .h) '
description: 針對月曆控制項設定目前選取的日期。 如果指定的日期不在 view 中，控制項會更新顯示，使其變成可供觀看。 您可以使用 MonthCal SetCurSel 宏明確地傳送此訊息 \_ 。
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- MCM_SETCURSEL message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceff48fbc4ffdb7446277d506c369e1bd89c92b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965115"
---
# <a name="mcm_setcursel-message"></a>MCM \_ SETCURSEL 訊息

針對月曆控制項設定目前選取的日期。 如果指定的日期不在 view 中，控制項會更新顯示，使其變成可供觀看。 您可以使用 [**MonthCal \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的指標，其中包含要設定為目前選取範圍的日期。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。 如果套用至使用 [**MCS \_ 多重選**](month-calendar-control-styles.md) 樣式的月曆控制項，此訊息將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[月曆控制項中的時間](month-calendar-controls.md)
</dt> </dl>

 

