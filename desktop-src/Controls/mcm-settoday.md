---
title: 'MCM_SETTODAY 訊息 (Commctrl .h) '
description: 設定 \ 0034; today \ 0034;月曆控制項的選取專案。 您可以使用 MonthCal SetToday 宏明確地傳送此訊息 \_ 。
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- MCM_SETTODAY 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea32e9ffc4d987ebf7d94e4508fbf7a057dbb5fe1115fea54ff82095f9d95938
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005301"
---
# <a name="mcm_settoday-message"></a>MCM \_ SETTODAY 訊息

設定月曆控制項的 "today" 選項。 您可以使用 [**MonthCal \_ SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的指標，其中包含要設定為控制項「今天」選取專案的日期。 如果這個參數設定為 **Null**，控制項會返回預設設定。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用此訊息的傳回值。

## <a name="remarks"></a>備註

如果 "today" 選項設定為預設值以外的任何日期，則適用下列條件：

-   當時間通過當日的午夜時，此控制項將不會自動更新「今天」選取範圍。
-   控制項不會根據地區設定變更自動更新其顯示。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[月曆控制項中的時間](month-calendar-controls.md)
</dt> </dl>

 

