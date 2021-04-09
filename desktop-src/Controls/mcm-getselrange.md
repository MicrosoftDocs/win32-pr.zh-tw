---
title: 'MCM_GETSELRANGE 訊息 (Commctrl .h) '
description: 抓取代表使用者目前所選取日期範圍上限和下限的日期資訊。 您可以使用 MonthCal GetSelRange 宏明確地傳送此訊息 \_ 。
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- MCM_GETSELRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934199"
---
# <a name="mcm_getselrange-message"></a>MCM \_ GETSELRANGE 訊息

抓取代表使用者目前所選取日期範圍上限和下限的日期資訊。 您可以使用 [**MonthCal \_ GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標，會接收使用者選取範圍的下限和上限。 下限和上限分別放在 *lprgSysTimeArray* \[ 0 \] 和 *lprgSysTimeArray* \[ 1 中 \] 。 此參數必須是有效的位址，而且不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。 **MCM \_** 如果套用至不使用 [**MCS \_ 多重選**](month-calendar-control-styles.md)樣式的月曆控制項，GETSELRANGE 將會失敗。

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

 

