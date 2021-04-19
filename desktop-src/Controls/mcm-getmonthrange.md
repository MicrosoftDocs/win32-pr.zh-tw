---
title: 'MCM_GETMONTHRANGE 訊息 (Commctrl .h) '
description: 使用代表月曆控制項顯示之最高和最低限制的 SYSTEMTIME 結構) ，抓取日期資訊 (。 您可以使用 MonthCal GetMonthRange 宏明確地傳送此訊息 \_ 。
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- MCM_GETMONTHRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022ca7e05cc0c69cd32f6ad92531420cdaed7c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965125"
---
# <a name="mcm_getmonthrange-message"></a>MCM \_ GETMONTHRANGE 訊息

使用代表月曆控制項顯示之最高和最低限制的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 結構) ，抓取日期資訊 (。 您可以使用 [**MonthCal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，指定要抓取範圍限制的範圍。 此值必須是下列其中一項：



| 值                                                                                                                                                      | 意義                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <dt>**GMR \_ DAYSTATE**</dt> </dl> | 包含只部分顯示之可見範圍的前置和尾端月份。 <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <dt>**GMR \_ 可見**</dt> </dl>    | 只包含完全顯示的月份。 <br/>                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標，會接收 *wParam* 所指定之範圍的下限和上限。 下限和上限分別放在 *lprgSysTimeArray* \[ 0 \] 和 *lprgSysTimeArray* \[ 1 中 \] 。 此參數必須是有效的位址，而且不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 INT 值，代表 *lParam* 所傳回的兩項限制的範圍（以月為單位）。

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

 

