---
description: 包含 pin 的目前信號產生狀態。
ms.assetid: 07D76F8D-C5B5-4500-BFA2-452989868027
title: 'PWM_PIN_IS_STARTED_OUTPUT 結構 (Pwm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_IS_STARTED_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 11350c3bb0fbec0f05ab3153c339f8fa30baeed5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972540"
---
# <a name="pwm_pin_is_started_output-structure"></a>PWM \_ PIN \_ 已 \_ 啟動 \_ 輸出結構

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

包含 pin 的目前信號產生狀態。

## <a name="syntax"></a>語法


```C++
typedef struct _PWM_PIN_IS_STARTED_OUTPUT {
  BOOLEAN IsStarted;
} PWM_PIN_IS_STARTED_OUTPUT;
```



## <a name="members"></a>成員

<dl> <dt>

**IsStarted**
</dt> <dd>

釘選目前信號產生狀態。 True 值表示已啟動 pin。 False 值表示已停止 pin。

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

[**已 \_ 啟動 IOCTL PWM \_ 釘選 \_ \_**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_IS\_STARTED**)
</dt> </dl>

 

 




