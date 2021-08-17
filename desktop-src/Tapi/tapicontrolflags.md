---
description: 多個方法會使用 TAPIControlFlags 列舉來指出指定的屬性是以自動或手動方式控制。
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: 'TAPIControlFlags 列舉 (Ipmsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 278cc2328335409d4ffcc95ea136826d121acd57776f98aaad947c8fb9ee5d93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139801"
---
# <a name="tapicontrolflags-enumeration"></a>TAPIControlFlags 列舉

\[此列舉無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

多個方法會使用 **TAPIControlFlags** 列舉來指出指定的屬性是以自動或手動方式控制。

## <a name="syntax"></a>Syntax


```C++
} TAPIControlFlags;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl \_ 旗標 \_ 無**
</dt> <dd>

TAPI 沒有屬性的控制旗標。

</dd> <dt>

<span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**\_自動 TAPIControl 旗標 \_**
</dt> <dd>

屬性會自動受到控制。

</dd> <dt>

<span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**TAPIControl \_ 旗標 \_ 手冊**
</dt> <dd>

屬性是以手動方式控制。

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
</dt> <dt>

[**ITAudioSettings：： GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings：： Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings：： Set**](itaudiosettings-set.md)
</dt> <dt>

[**ITCallQualityControl：： GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl：： Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl：： Set**](itcallqualitycontrol-set.md)
</dt> <dt>

[**ITStreamQualityControl：： GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl：： Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl：： Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




