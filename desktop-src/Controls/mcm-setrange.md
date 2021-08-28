---
title: 'MCM_SETRANGE 訊息 (Commctrl .h) '
description: 設定月曆控制項的最小和最大允許日期。 您可以使用 MonthCal SetRange 宏明確地傳送此訊息 \_ 。
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- MCM_SETRANGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c66e9cca17aabd93bfba896d361da6b90eab0c5c21fc4d50ec3c81a9eba5ccd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319248"
---
# <a name="mcm_setrange-message"></a>MCM \_ SETRANGE 訊息

設定月曆控制項的最小和最大允許日期。 您可以使用 [**MonthCal \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

旗標值，指定要設定的日期限制。 此值必須是下列其中一項或兩項：



| 值                                                                                                                                          | 意義                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ MAX**</dt> </dl> | 已設定允許的最大日期。 *LpSysTimeArray* 1 的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構 \[ \] 必須包含日期資訊。 <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ 分鐘**</dt> </dl> | 已設定允許的最小日期。 位於 *lpSysTimeArray* 0 的 [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構 \[ \] 必須包含日期資訊。 <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的雙元素陣列的指標，其中包含日期限制。  \[ 如果指定了 GDTR MAX，則上限必須在 lpSysTimeArray 1 中 \] \_ ，  \[ \] 如果指定了 GDTR MIN，則 lpSysTimeArray 0 必須包含最小限制 \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

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

 

