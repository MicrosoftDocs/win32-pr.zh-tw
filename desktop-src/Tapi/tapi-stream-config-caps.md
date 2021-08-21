---
description: TAPI \_ 串流設定 \_ \_ CAPS 結構包含影片或音訊串流設定資訊。
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: 'TAPI_STREAM_CONFIG_CAPS 結構 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbbb3b3ec72cc99810311cc510e36c2adc8242e2b3d98b321fd8bc8c6a9ab4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002646"
---
# <a name="tapi_stream_config_caps-structure"></a>TAPI \_ 串流 \_ 設定 \_ CAPS 結構

\[此結構無法在 Windows Vista、Windows Server 2008 及後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

**TAPI \_ 串流設定 \_ \_ CAPS** 結構包含影片或音訊串流設定資訊。

## <a name="syntax"></a>語法


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a>成員

<dl> <dt>

**CapsType**
</dt> <dd>

定義聯集成員是否包含影片或音訊資訊。

</dd> <dt>

**VideoCap**
</dt> <dd>

包含影片串流功能的 [**TAPI \_ 影片 \_ 串流設定 \_ \_ cap**](tapi-video-stream-config-caps.md) 結構。

</dd> <dt>

**AudioCap**
</dt> <dd>

包含音訊串流功能的 [**TAPI \_ 音訊 \_ 串流設定 \_ \_ cap**](tapi-audio-stream-config-caps.md) 結構。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                       |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITFormatControl::GetStreamCaps**](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[**StreamConfigCapsType**](streamconfigcapstype.md)
</dt> <dt>

[**TAPI \_ 影片 \_ 串流 \_ 設定 \_ 上限**](tapi-video-stream-config-caps.md)
</dt> <dt>

[**TAPI \_ 音訊 \_ 串流 \_ 設定 \_ CAP**](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




