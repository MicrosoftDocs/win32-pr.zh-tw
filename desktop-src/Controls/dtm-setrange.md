---
title: 'DTM_SETRANGE 訊息 (Commctrl .h) '
description: 設定日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。 您可以明確地傳送此訊息，或使用 DateTime \_ SetRange 宏。
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- DTM_SETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686172"
---
# <a name="dtm_setrange-message"></a>DTM \_ SETRANGE 訊息

設定日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。 您可以明確地傳送此訊息，或使用 [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，指定有效的範圍值。 這個參數可以是下列值的組合：



| 值                                                                                                                                          | 意義                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ 分鐘**</dt> </dl> | [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構陣列中的第一個元素是有效的，而且將用來設定允許的最小系統時間。<br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ MAX**</dt> </dl> | [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構陣列中的第二個元素是有效的，而且將用來設定允許的最大系統時間。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標。 **SYSTEMTIME** 陣列的第一個元素包含允許的最小時間。 **SYSTEMTIME** 陣列的第二個元素包含允許的最大時間。 不需要填滿未在 *wParam* 參數中指定的陣列元素。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零，否則傳回零。

## <a name="remarks"></a>備註

日期和時間選擇器只會顯示落在指定範圍內的日期/時間，防止使用者選取超出範圍的日期和時間。 如果 [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) 訊息指定超出範圍的日期和時間，它將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

