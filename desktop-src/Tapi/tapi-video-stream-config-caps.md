---
description: '\_ \_ \_ \_ \_ \_ \_ 當 CapsType 成員設定為 StreamConfigCapsType 聯集的 VideoCap 成員時，TAPI 串流設定 caps 結構會包含 tapi 影片串流設定 caps 結構。'
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: 'TAPI_VIDEO_STREAM_CONFIG_CAPS 結構 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999674"
---
# <a name="tapi_video_stream_config_caps-structure"></a>TAPI \_ 影片 \_ 串流 \_ 設定 \_ CAPS 結構

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用此結構。 RTC 用戶端 API 提供類似的功能。\]

當 **CapsType** 成員設定為 [**StreamConfigCapsType**](streamconfigcapstype.md)聯集的 **VideoCap** 成員時，tapi [**\_ 串流 \_ \_**](tapi-stream-config-caps.md)設定 caps 結構會包含 **tapi \_ 影片 \_ 串流設定 \_ \_ caps** 結構。

## <a name="syntax"></a>語法


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>成員

<dl> <dt>

**說明**
</dt> <dd>

顯示給應用程式使用者之音訊串流設定類型的易記描述。

</dd> <dt>

**VideoStandard**
</dt> <dd>

使用的影片標準。

</dd> <dt>

**InputSize**
</dt> <dd>

輸入框架的大小。

</dd> <dt>

**MinCroppingSize**
</dt> <dd>

最小裁剪大小。

</dd> <dt>

**MaxCroppingSize**
</dt> <dd>

裁剪大小上限。

</dd> <dt>

**CropGranularityX**
</dt> <dd>

沿著 X 軸允許裁剪的資料細微性。

</dd> <dt>

**CropGranularityY**
</dt> <dd>

沿著 y 軸允許裁剪的資料細微性。

</dd> <dt>

**CropAlignX**
</dt> <dd>

X 軸裁剪的對齊方式。

</dd> <dt>

**CropAlignY**
</dt> <dd>

Y 軸裁剪的對齊方式。

</dd> <dt>

**MinOutputSize**
</dt> <dd>

影片視窗的最小結果大小。

</dd> <dt>

**MaxOutputSize**
</dt> <dd>

影片視窗的結果大小上限。

</dd> <dt>

**OutputGranularityX**
</dt> <dd>

沿著 X 軸輸出大小的資料細微性。

</dd> <dt>

**OutputGranularityY**
</dt> <dd>

沿著 y 軸的輸出大小的資料細微性。

</dd> <dt>

**StretchTapsX**
</dt> <dd>

沿著 X 軸伸展。

</dd> <dt>

**StretchTapsY**
</dt> <dd>

沿著 y 軸伸展。

</dd> <dt>

**ShrinkTapsX**
</dt> <dd>

沿著 X 軸壓縮。

</dd> <dt>

**ShrinkTapsY**
</dt> <dd>

沿著 y 軸壓縮。

</dd> <dt>

**MinFrameInterval**
</dt> <dd>

最小影片畫面間隔。

</dd> <dt>

**MaxFrameInterval**
</dt> <dd>

最大影片畫面間隔。

</dd> <dt>

**MinBitsPerSecond**
</dt> <dd>

每秒的最小位數。

</dd> <dt>

**MaxBitsPerSecond**
</dt> <dd>

每秒最大位數。

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

 

 




