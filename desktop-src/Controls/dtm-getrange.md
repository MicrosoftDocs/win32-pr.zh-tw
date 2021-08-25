---
title: 'DTM_GETRANGE 訊息 (Commctrl .h) '
description: 取得日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。 您可以明確地傳送此訊息，或使用 DateTime \_ GetRange 宏。
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- DTM_GETRANGE 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9c0c90780e4bcd35da2d410f7b4743547cbd8d31ac06293c411f2415e4e408
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877948"
---
# <a name="dtm_getrange-message"></a>DTM \_ GETRANGE 訊息

取得日期和時間選擇器 (DTP) 控制項的最小和最大允許系統時間。 您可以明確地傳送此訊息，或使用 [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) 宏。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 GDTR  \_ MIN 或 GDTR MAX 組合的 DWORD 值 \_ 。 如果設定 GDTR MIN， [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) 陣列的第一個元素包含最小允許時間 \_ 。 如果設定 GDTR MAX， **SYSTEMTIME** 陣列的第二個元素會包含最大允許時間 \_ 。

## <a name="remarks"></a>備註

日期和時間選擇器只會顯示落在指定範圍內的日期/時間，防止使用者選取超出範圍的日期和時間。 如果 [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) 訊息指定超出範圍的日期和時間，它將會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

