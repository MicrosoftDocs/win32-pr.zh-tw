---
title: 'WINBIO_EXTENDED_SENSOR_INFO 結構 (Winbio \_ 類型 .h) '
description: 包含生物特徵辨識設備之感應器介面卡的功能和註冊需求相關資訊。
ms.assetid: 37D8BC57-F68D-487A-98B0-94D62CC091C2
keywords:
- WINBIO_EXTENDED_SENSOR_INFO 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EXTENDED_SENSOR_INFO 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_SENSOR_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c535ef56eeade897aac3c1d0503477da406935b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934022"
---
# <a name="winbio_extended_sensor_info-structure"></a>WINBIO \_ 擴充的 \_ 感應器 \_ 資訊結構

包含生物特徵辨識設備之感應器介面卡的功能和註冊需求相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_EXTENDED_SENSOR_INFO {
  WINBIO_CAPABILITIES   GenericSensorCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } FacialFeatures;
    struct {
      ULONG32 Reserved;
    } Fingerprint;
    struct {
      RECT               FrameSize;
      POINT              FrameOffset;
      WINBIO_ORIENTATION MandatoryOrientation;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_SENSOR_INFO, *PWINBIO_EXTENDED_SENSOR_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**GenericSensorCapabilities**
</dt> <dd>

連接到特定生物識別單位之感應器元件的一般功能。

</dd> <dt>

**因素**
</dt> <dd>

此結構包含感應器介面卡功能和註冊需求相關資訊的生物特徵辨識單位類型。 例如，如果 **因素** 成員的值是 **WINBIO \_ 類型 \_ 指紋**， **WINBIO \_ 擴充 \_ 感應器 \_ 資訊** 結構會套用至指紋辨識器，並在 **專屬** 中包含相關資訊。

</dd> <dt>

**特定**
</dt> <dd>

與特定生物特徵辨識因素相關之生物特徵辨識設備的感應器介面卡功能和註冊需求相關資訊。

<dl> <dt>

**Null**
</dt> <dd>

保留的。 必須為零。

</dd> <dt>

**FacialFeatures**
</dt> <dd>

與臉部特徵相關之生物特徵辨識設備的感應器介面卡功能和註冊需求相關資訊。

<dl> <dt>

**FrameSize**
</dt> <dd>

攝影機框架的大小，以圖元為 **單位的長度****和寬度**（以圖元為單位）。 [](/previous-versions//dd162897(v=vs.85)) 點 (0，0) 代表框架的左上角。

</dd> <dt>

**FrameOffset**
</dt> <dd>

攝影機的相機框架距離（以圖元為單位）。 值為 (0，0) 表示臉部和攝影機的相機框架完全重迭。

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

相機的慣用方向。

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

與指紋模式相關之生物特徵辨識設備的感應器介面卡功能和註冊需求相關資訊。

<dl> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> </dl> </dd> <dt>

**虹膜**
</dt> <dd>

與鳶尾花模式相關的生物特徵辨識單位之感應器介面卡功能和註冊需求的相關資訊。

<dl> <dt>

**FrameSize**
</dt> <dd>

攝影機框架的大小，以圖元為 **單位的長度****和寬度**（以圖元為單位）。 [](/previous-versions//dd162897(v=vs.85)) 點 (0，0) 代表框架的左上角。

</dd> <dt>

**FrameOffset**
</dt> <dd>

鳶尾花攝影機框架的距離（以圖元為單位）。 值為 (0，0) 表示鳶尾花和攝影機的相機框架完全重迭。

</dd> <dt>

**MandatoryOrientation**
</dt> <dd>

相機的慣用方向。

</dd> </dl> </dd> <dt>

**語音**
</dt> <dd>

與語音模式相關之生物特徵辨識單位的感應器介面卡功能和註冊需求相關資訊。

<dl> <dt>

**已保留**
</dt> <dd>

保留的。

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WINBIO \_ 功能常數**](winbio-capability-constants.md)
</dt> <dt>

[**WINBIO \_ 生物特徵辨識 \_ 類型常數**](winbio-biometric-type-constants.md)
</dt> <dt>

[**WINBIO \_ 方向常數**](winbio-orientation-constants.md)
</dt> </dl>

 

