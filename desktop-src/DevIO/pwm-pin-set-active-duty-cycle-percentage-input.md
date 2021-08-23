---
description: 包含在脈衝寬度調製 (PWM) 控制器的 pin 或通道所需的工作週期百分比。
ms.assetid: CA699703-2D9B-4841-99AD-9C27FF428394
title: 'PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT 結構 (Pwm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: ca6b2ee6aa4d4d2da3f94aa7cc471de12c1f8040b597edf568bf061c8e392aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758848"
---
# <a name="pwm_pin_set_active_duty_cycle_percentage_input-structure"></a>PWM 釘選設定使用中的工作 \_ \_ \_ \_ \_ 週期 \_ 百分比 \_ 輸入結構

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

包含在脈衝寬度調製 (PWM) 控制器的 pin 或通道所需的工作週期百分比。

## <a name="syntax"></a>語法


```C++
typedef struct _PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_SET_ACTIVE_DUTY_CYCLE_PERCENTAGE_INPUT;
```



## <a name="members"></a>成員

<dl> <dt>

**百分比**
</dt> <dd>

所需的 PWM 信號工作週期，以 PWM 百分比表示，也 \_ 就是 ULONGLONG 值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                      |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                             |
| 最小 KMDF 版本<br/>     | 1.19<br/>                                                                                  |
| 最小的 UMDF 版本<br/>     | 2.19<br/>                                                                                  |
| 標頭<br/>                   | <dl> <dt>Pwm (包含 Pwm) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOCTL \_ PWM \_ 釘選有效的工作 \_ \_ \_ \_ 週期 \_ 百分比**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_SET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




