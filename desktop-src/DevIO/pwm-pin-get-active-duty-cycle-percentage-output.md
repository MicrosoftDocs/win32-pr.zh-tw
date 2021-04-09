---
description: 包含以脈衝寬度調整 (PWM) 控制器的 pin 或通道目前的工作週期百分比。
ms.assetid: 09C0232A-DF5C-4A1C-8138-D3D65E45731B
title: 'PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT 結構 (Pwm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 607fcb1ab429e7cbe9aee593f75d48f0f9d308bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110681"
---
# <a name="pwm_pin_get_active_duty_cycle_percentage_output-structure"></a>PWM \_ PIN \_ 取得 \_ 主動式的工作 \_ \_ 週期 \_ 百分比 \_ 輸出結構

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

包含以脈衝寬度調整 (PWM) 控制器的 pin 或通道目前的工作週期百分比。

## <a name="syntax"></a>語法


```C++
typedef struct _PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT {
  PWM_PERCENTAGE Percentage;
} PWM_PIN_GET_ACTIVE_DUTY_CYCLE_PERCENTAGE_OUTPUT;
```



## <a name="members"></a>成員

<dl> <dt>

**百分比**
</dt> <dd>

目前的 PWM 信號工作週期，以 PWM 百分比表示，也 \_ 就是 ULONGLONG 值。

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

[**IOCTL \_ PWM PIN 取得使用中的工作 \_ \_ \_ \_ \_ 週期 \_ 百分比**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_ACTIVE\_DUTY\_CYCLE\_PERCENTAGE**)
</dt> </dl>

 

 




