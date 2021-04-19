---
description: TAPI 串流設定 CAPS 結構會使用 StreamConfigCapsType 列舉 \_ 類型 \_ \_ 作為參數，指出是否牽涉到音訊或影片串流。
ms.assetid: c3eec6b2-ce3b-49b1-a0ba-f450d60a1477
title: 'StreamConfigCapsType 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14649edb7e451cdc7d955f2028a77c247148182b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984890"
---
# <a name="streamconfigcapstype-enumeration"></a>StreamConfigCapsType 列舉

\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

[**TAPI \_ 串流設定 \_ \_ CAPS**](tapi-stream-config-caps.md)結構會使用 **StreamConfigCapsType** 列舉類型作為參數，指出是否牽涉到音訊或影片串流。

## <a name="syntax"></a>Syntax


```C++
} StreamConfigCapsType;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**AudioStreamConfigCaps**
</dt> <dd>

音訊串流設定。

</dd> <dt>

<span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**VideoStreamConfigCaps**
</dt> <dd>

影片串流設定。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                       |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TAPI \_ 串流 \_ 設定 \_ CAP**](tapi-stream-config-caps.md)
</dt> </dl>

 

 




