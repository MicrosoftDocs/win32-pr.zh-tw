---
title: 'MCM_SETFIRSTDAYOFWEEK 訊息 (Commctrl .h) '
description: 設定月曆控制項的每週第一天。 您可以使用 MonthCal SetFirstDayOfWeek 宏明確地傳送此訊息 \_ 。
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- MCM_SETFIRSTDAYOFWEEK 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e34732257c18acceec3fd7db9807753e9a930e106198b33a0dd61dc27a33eef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077108"
---
# <a name="mcm_setfirstdayofweek-message"></a>MCM \_ SETFIRSTDAYOFWEEK 訊息

設定月曆控制項的每週第一天。 您可以使用 [**MonthCal \_ SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>

**Int** 類型的值，代表要將哪一天設定為星期幾的第一天，其中0是星期一、1是星期二等等。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含兩個值的 **DWORD** 值。 如果第一周的第一天不等於地區設定 IFIRSTDAYOFWEEK，則最 **大的單字** 為非零值，否則為 \_ 零。 低字組是一個 INT 值，代表一周的前一天。

## <a name="remarks"></a>備註

如果一周的第一天設定為預設 (地區設定 IFIRSTDAYOFWEEK) 以外的任何值 \_ ，則此控制項不會根據地區設定變更自動更新第一天的變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





