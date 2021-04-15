---
title: 'MCM_SETDAYSTATE 訊息 (Commctrl .h) '
description: 設定當月月曆控制項中目前可見的所有月份的日期狀態。 您可以使用 MonthCal SetDayState 宏明確地傳送此訊息 \_ 。
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- MCM_SETDAYSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466801"
---
# <a name="mcm_setdaystate-message"></a>MCM \_ SETDAYSTATE 訊息

設定當月月曆控制項中目前可見的所有月份的日期狀態。 您可以使用 [**MonthCal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，指出 *lParam* 所指向陣列中的元素數目。

</dd> <dt>

*lParam* 
</dt> <dd>

[**MONTHDAYSTATE**](monthdaystate.md)值陣列的指標，定義月曆控制項在其顯示中每天的繪製方式。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

應用程式可以藉由傳送此訊息來明確設定日狀態資訊，但在行事曆的不同部分滾動查看時，狀態將不會保存。 日期狀態資訊通常是為了回應 [MCN \_ GETDAYSTATE](mcn-getdaystate.md) 通知碼而設定，每當控制項需要重新整理時，就會傳送此通知碼。

*LParam* 的陣列必須包含的元素數目，與下列宏所傳回的值相同：

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

請記住， *lParam* 中的陣列必須包含 [**MONTHDAYSTATE**](monthdaystate.md) 值，而這些值會對應到目前在控制項顯示中的所有月份（以時間順序排列）。 這包括兩個月，可能會在第一個月之前和最後一個月之後部分顯示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用月曆控制項](using-month-calendar-controls.md)
</dt> </dl>

 

 





