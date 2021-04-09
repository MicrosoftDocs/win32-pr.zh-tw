---
title: 'MCM_GETRANGE 訊息 (Commctrl .h) '
description: 抓取月曆控制項設定的最小和最大允許日期。 您可以使用 MonthCal GetRange 宏明確地傳送此訊息 \_ 。
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- MCM_GETRANGE message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c757c046b88479072eb0771ecbf3f7fb79cdb31b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844287"
---
# <a name="mcm_getrange-message"></a>MCM \_ GETRANGE 訊息

抓取月曆控制項設定的最小和最大允許日期。 您可以使用 [**MonthCal \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構的兩個元素陣列的指標，會接收日期限制資訊。 最小限制設定為 *lprgSysTimeArray* \[ 0 \] ，而 *lprgSysTimeArray* 1 則會 \[ 收到上限 \] 。 如果任一個元素設定為全部零，則不會針對月曆控制項設定對應的限制。 此參數必須是有效的位址，而且不可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回可為零的 **DWORD** (沒有設定任何限制) 或下列值的組合，這些值會指定限制資訊：



| 傳回碼                                                                              | Description                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GDTR \_ MAX**</dt> </dl> | 為控制項設定了上限，*lprgSysTimeArray* \[0 \] 有效，且包含適用的日期資訊。 <br/> |
| <dl> <dt>**GDTR \_ 分鐘**</dt> </dl> | 針對控制項設定的最小限制為;*lprgSysTimeArray* \[1 \] 是有效的，而且包含適用的日期資訊。 <br/> |



 

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

 

