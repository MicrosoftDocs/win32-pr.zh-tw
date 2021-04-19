---
description: ITCallQualityControl：： GetRange、ITCallQualityControl：： Get 和 ITCallQualityControl：： Set 方法會使用 CallQualityProperty 列舉來指出要處理的呼叫品質屬性。
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: 'CallQualityProperty 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998855"
---
# <a name="callqualityproperty-enumeration"></a>CallQualityProperty 列舉

\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

[**ITCallQualityControl：： GetRange**](itcallqualitycontrol-getrange.md)、 [**ITCallQualityControl：： Get**](itcallqualitycontrol-get.md)和 [**ITCallQualityControl：： Set**](itcallqualitycontrol-set.md)方法會使用 **CallQualityProperty** 列舉來指出要處理的呼叫品質屬性。

## <a name="syntax"></a>Syntax


```C++
} CallQualityProperty;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality \_ ControlInterval**
</dt> <dd>

控制間隔。

</dd> <dt>

<span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality \_ ConfBitrate**
</dt> <dd>

會議的位元速率。

</dd> <dt>

<span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality \_ MaxInputBitrate**
</dt> <dd>

最大輸入位速率。

</dd> <dt>

<span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality \_ CurrInputBitrate**
</dt> <dd>

目前的輸入位速度。

</dd> <dt>

<span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality \_ MaxOutputBitrate**
</dt> <dd>

最大輸出位元速率。

</dd> <dt>

<span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality \_ CurrOutputBitrate**
</dt> <dd>

目前的輸出位元速率。

</dd> <dt>

<span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality \_ >maxcpuload**
</dt> <dd>

最大 CPU 負載。

</dd> <dt>

<span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality \_ CurrCPULoad**
</dt> <dd>

目前的 CPU 負載。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                       |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITCallQualityControl：： GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl：： Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl：： Set**](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




