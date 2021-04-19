---
description: '\_ \_ \_ \_ \_ \_ \_ 當 CapsType 成員設定為 StreamConfigCapsType 聯集的 AudioCap 成員時，tapi 音訊串流設定 caps 結構會包含在 tapi 串流設定的 cap 結構中。'
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: 'TAPI_AUDIO_STREAM_CONFIG_CAPS 結構 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982591"
---
# <a name="tapi_audio_stream_config_caps-structure"></a>TAPI \_ 音訊 \_ 串流 \_ 設定 \_ CAPS 結構

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用此結構。 RTC 用戶端 API 提供類似的功能。\]

當 **CapsType** 成員設定為 [**StreamConfigCapsType**](streamconfigcapstype.md)聯集的 **AudioCap** 成員時，tapi **\_ 音訊 \_ 串流設定 \_ \_ caps** 結構會包含在 [**tapi \_ 串流 \_ \_**](tapi-stream-config-caps.md)設定的 cap 結構中。

## <a name="syntax"></a>語法


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>成員

<dl> <dt>

**說明**
</dt> <dd>

顯示給應用程式使用者之音訊串流設定類型的易記描述。

</dd> <dt>

**MinimumChannels**
</dt> <dd>

與資料流程相關聯的通道數目下限。

</dd> <dt>

**MaximumChannels**
</dt> <dd>

與資料流程相關聯的通道數目上限。

</dd> <dt>

**ChannelsGranularity**
</dt> <dd>

通道計數的資料細微性。

</dd> <dt>

**MinimumBitsPerSample**
</dt> <dd>

每個樣本的最小位數。

</dd> <dt>

**MaximumBitsPerSample**
</dt> <dd>

每個樣本的位數上限。

</dd> <dt>

**BitsPerSampleGranularity**
</dt> <dd>

每個樣本值的位細微性。

</dd> <dt>

**MinimumSampleFrequency**
</dt> <dd>

最小取樣頻率。

</dd> <dt>

**MaximumSampleFrequency**
</dt> <dd>

最大取樣頻率。

</dd> <dt>

**SampleFrequencyGranularity**
</dt> <dd>

取樣頻率值的資料細微性。

</dd> <dt>

**MinimumAvgBytesPerSec**
</dt> <dd>

每秒的最小平均位元組數。

</dd> <dt>

**MaximumAvgBytesPerSec**
</dt> <dd>

每秒最大的平均位元組數。

</dd> <dt>

**AvgBytesPerSecGranularity**
</dt> <dd>

每秒位元組數值的資料細微性。

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

 

 




