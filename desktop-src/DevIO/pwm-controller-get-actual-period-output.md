---
description: 包含脈衝寬度調製 (PWM) 控制器的有效輸出信號期間。
ms.assetid: 280F564F-FF7F-4121-B726-9F9AF9E98EB7
title: 'PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT 結構 (Pwm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: f63057299a8ef37ed1b38151958d2e0061ad2727
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688848"
---
# <a name="pwm_controller_get_actual_period_output-structure"></a>PWM \_ 控制器 \_ 取得 \_ 實際 \_ 期間 \_ 輸出結構

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

包含脈衝寬度調製 (PWM) 控制器的有效輸出信號期間。

## <a name="syntax"></a>語法


```C++
typedef struct _PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT {
  PWM_PERIOD ActualPeriod;
} PWM_CONTROLLER_GET_ACTUAL_PERIOD_OUTPUT;
```



## <a name="members"></a>成員

<dl> <dt>

**ActualPeriod**
</dt> <dd>

在控制器輸出通道上測量的有效輸出信號週期。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                             |
| 最小 KMDF 版本<br/>     | 1.19<br/>                                                                                  |
| 最小的 UMDF 版本<br/>     | 2.19<br/>                                                                                  |
| 標頭<br/>                   | <dl> <dt>Pwm (包含 Pwm) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOCTL \_ PWM \_ 控制器 \_ 取得 \_ 實際 \_ 期間**](https://www.bing.com/search?q=**IOCTL\_PWM\_CONTROLLER\_GET\_ACTUAL\_PERIOD**)
</dt> </dl>

 

 




