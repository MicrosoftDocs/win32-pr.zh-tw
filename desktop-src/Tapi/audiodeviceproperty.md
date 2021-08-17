---
description: ITAudioDeviceControl：： GetRange、ITAudioDeviceControl：： Get 和 ITAudioDeviceControl：： Set 方法會使用 AudioDeviceProperty 列舉來指出要處理的屬性。
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: 'AudioDeviceProperty 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a634caa627f5d518e8783ce056e89a69931aa981466754a9d320f36787186f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948790"
---
# <a name="audiodeviceproperty-enumeration"></a>AudioDeviceProperty 列舉

\[此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

[**ITAudioDeviceControl：： GetRange**](itaudiodevicecontrol-getrange.md)、 [**ITAudioDeviceControl：： Get**](itaudiodevicecontrol-get.md)和 [**ITAudioDeviceControl：： Set**](itaudiodevicecontrol-set.md)方法會使用 **AudioDeviceProperty** 列舉來指出要處理的屬性。

## <a name="syntax"></a>Syntax


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice \_ DuplexMode**
</dt> <dd>

指出正在設定或抓取裝置的雙工模式。

</dd> <dt>

<span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice \_ AutomaticGainControl**
</dt> <dd>

指出正在設定或抓取裝置的自動增益控制。

</dd> <dt>

<span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice \_ AcousticEchoCancellation**
</dt> <dd>

指出正在設定或抓取裝置的聲場回顯取消屬性。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3。1<br/>                                                       |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITAudioDeviceControl：： GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**ITAudioDeviceControl：： Get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**ITAudioDeviceControl：： Set**](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




