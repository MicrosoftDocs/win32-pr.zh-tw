---
title: 'MCM_GETMONTHDELTA 訊息 (Commctrl .h) '
description: 抓取月曆控制項的滾動速率。 捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。 您可以使用 MonthCal GetMonthDelta 宏明確地傳送此訊息 \_ 。
ms.assetid: 6db02993-b22c-430f-8928-8bd5768b2151
keywords:
- MCM_GETMONTHDELTA 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c13a13d75a1655c1082b4b4611517915be14e27b0fb1c5f94fb5a17f6db973e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319608"
---
# <a name="mcm_getmonthdelta-message"></a>MCM \_ GETMONTHDELTA 訊息

抓取月曆控制項的滾動速率。 捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。 您可以使用 [**MonthCal \_ GetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthdelta) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果先前使用 [**MCM \_ SETMONTHDELTA**](mcm-setmonthdelta.md) 訊息設定了月份差異，則會傳回代表月曆目前滾動率的 INT 值。 如果先前未使用 **MCM \_ SETMONTHDELTA** 訊息來設定月份差異，或重設為預設的月差異，則會傳回 INT 值，代表目前可見的月數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





