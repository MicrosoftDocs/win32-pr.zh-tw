---
description: ITStreamQualityControl：： GetRange、ITStreamQualityControl：： Get 和 ITStreamQualityControl：： Set 方法所使用的 StreamQualityProperty 列舉，表示要處理的資料流程品質屬性。
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: 'StreamQualityProperty 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f552641cd0847bb3ff8eec9d528a03171a78c2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980245"
---
# <a name="streamqualityproperty-enumeration"></a>StreamQualityProperty 列舉

\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

[**ITStreamQualityControl：： GetRange**](itstreamqualitycontrol-getrange.md)、 [**ITStreamQualityControl：： Get**](itstreamqualitycontrol-get.md)和 [**ITStreamQualityControl：： Set**](itstreamqualitycontrol-set.md)方法所使用的 **StreamQualityProperty** 列舉，表示要處理的資料流程品質屬性。

## <a name="syntax"></a>Syntax


```C++
} StreamQualityProperty;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality \_ MaxBitrate**
</dt> <dd>

最大位元速率。

</dd> <dt>

<span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality \_ CurrBitrate**
</dt> <dd>

最小位元速率。

</dd> <dt>

<span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality \_ MinFrameInterval**
</dt> <dd>

最大幀間隔。

</dd> <dt>

<span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality \_ AvgFrameInterval**
</dt> <dd>

最小框架間隔。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                       |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITStreamQualityControl：： GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl：： Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl：： Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




