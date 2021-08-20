---
title: 'MCM_SETMONTHDELTA 訊息 (Commctrl .h) '
description: 設定月曆控制項的滾動速率。 捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。 您可以使用 MonthCal SetMonthDelta 宏明確地傳送此訊息 \_ 。
ms.assetid: 2d01b95f-3be8-4548-80b5-ac01d3e49e9f
keywords:
- MCM_SETMONTHDELTA 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- MCM_SETMONTHDELTA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a148bac8ee28d4e3ebeb370d9fcacb678730bc77baac0b42f3f14b8f65a57e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118005379"
---
# <a name="mcm_setmonthdelta-message"></a>MCM \_ SETMONTHDELTA 訊息

設定月曆控制項的滾動速率。 捲軸速率是當使用者按一下滾動按鈕時，控制項移動其顯示的月數。 您可以使用 [**MonthCal \_ SetMonthDelta**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmonthdelta) 宏明確地傳送此訊息。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

值，代表要設定為控制項滾動速率的月數。 如果此值為零，則會將月份差異重設為預設值，也就是顯示在控制項中的月份數。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回代表前一個滾動速率的 INT 值。 如果之前未設定捲軸速率，則傳回值為零。

## <a name="remarks"></a>備註

PAGE UP 和 PAGE DOWN 鍵，VK \_ 上 \_ 一步和 VK 下一步，不論顯示的月份數或 **MCM \_ SETMONTHDELTA** 設定的值為何，都會將選取的月份變更為1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





