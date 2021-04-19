---
description: ITAudioSettings：： GetRange、ITAudioSettings：： Get 和 ITAudioSettings：： Set 方法會使用 AudioSettingsProperty 列舉來指出要處理的音訊設定屬性。
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: 'AudioSettingsProperty 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759e3ca9d9559c35c64c117b9b84b1cee4a1fad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982639"
---
# <a name="audiosettingsproperty-enumeration"></a>AudioSettingsProperty 列舉

\[ 此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

[**ITAudioSettings：： GetRange**](itaudiosettings-getrange.md)、 [**ITAudioSettings：： Get**](itaudiosettings-get.md)和 [**ITAudioSettings：： Set**](itaudiosettings-set.md)方法會使用 **AudioSettingsProperty** 列舉來指出要處理的音訊設定屬性。

## <a name="syntax"></a>Syntax


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**
</dt> <dd>

信號設定屬性。

</dd> <dt>

<span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**
</dt> <dd>

無聲臨界值屬性。

</dd> <dt>

<span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**AudioSettings \_ 磁片區**
</dt> <dd>

Volume 屬性。

</dd> <dt>

<span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings \_ 餘額**
</dt> <dd>

餘額屬性。

</dd> <dt>

<span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings \_ 音量**
</dt> <dd>

音量屬性。

</dd> <dt>

<span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ 高音**
</dt> <dd>

高音屬性。

</dd> <dt>

<span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings \_ 低音**
</dt> <dd>

低音屬性。

</dd> <dt>

<span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings \_ Mono**
</dt> <dd>

Monaural 屬性。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                       |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITAudioSettings：： GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings：： Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings：： Set**](itaudiosettings-set.md)
</dt> </dl>

 

 




