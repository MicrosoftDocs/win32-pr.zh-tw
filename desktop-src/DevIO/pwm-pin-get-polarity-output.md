---
description: 包含要傳回的極性值。
ms.assetid: 432C10EF-AC08-4781-9BCA-A31E0DF12704
title: 'PWM_PIN_GET_POLARITY_OUTPUT 結構 (Pwm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PWM_PIN_GET_POLARITY_OUTPUT
api_type:
- HeaderDef
api_location:
- Pwm.h
ms.openlocfilehash: 7d4c3103663ceac65deff7744b0cf45a21a787959cc6e866bde5ac8673f7f64a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984428"
---
# <a name="pwm_pin_get_polarity_output-structure"></a>PWM \_ 針腳 \_ 取得 \_ 極性 \_ 輸出結構

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

包含要傳回的極性值。

## <a name="syntax"></a>語法


```C++
typedef struct _PWM_PIN_GET_POLARITY_OUTPUT {
  PWM_POLARITY Polarity;
} PWM_PIN_GET_POLARITY_OUTPUT;
```



## <a name="members"></a>成員

<dl> <dt>

**極性**
</dt> <dd>

作為 [**PWM \_ 極性**](/windows/desktop/api/Pwm/ne-pwm-pwm_polarity) 值的釘選或通道極性。 極性是主動高或主動低。

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

[**IOCTL \_ PWM \_ 圖釘 \_ 取得 \_ 極性**](https://www.bing.com/search?q=**IOCTL\_PWM\_PIN\_GET\_POLARITY**)
</dt> <dt>

[**PWM \_ 極性**](/windows/win32/api/pwm/ne-pwm-pwm_polarity)
</dt> </dl>

 

