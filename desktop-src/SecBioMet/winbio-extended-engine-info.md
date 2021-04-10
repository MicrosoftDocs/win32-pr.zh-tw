---
title: 'WINBIO_EXTENDED_ENGINE_INFO 結構 (Winbio \_ 類型 .h) '
description: 包含生物特徵辨識裝置引擎介面卡的功能和註冊需求相關資訊。
ms.assetid: 83586E04-24CA-4A39-836F-C80DB1508C71
keywords:
- WINBIO_EXTENDED_ENGINE_INFO 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EXTENDED_ENGINE_INFO 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENGINE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829bd0423ab6add41b17f59d308aea850c5b2f42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844319"
---
# <a name="winbio_extended_engine_info-structure"></a>WINBIO \_ 延伸 \_ 引擎 \_ 資訊結構

包含生物特徵辨識裝置引擎介面卡的功能和註冊需求相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_EXTENDED_ENGINE_INFO {
  WINBIO_CAPABILITIES   GenericEngineCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG GeneralSamples;
        ULONG Center;
        ULONG TopEdge;
        ULONG BottomEdge;
        ULONG LeftEdge;
        ULONG RightEdge;
      } EnrollmentRequirements;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
      struct {
        ULONG32 Null;
      } EnrollmentRequirements;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENGINE_INFO, *PWINBIO_EXTENDED_ENGINE_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**GenericEngineCapabilities**
</dt> <dd>

連接到特定生物識別單位之引擎元件的一般功能。

</dd> <dt>

**因素**
</dt> <dd>

此結構包含引擎介面卡功能和註冊需求相關資訊的生物特徵辨識單位類型。 例如，如果 **因素** 成員的值是 **WINBIO \_ 類型 \_ 指紋**，則 **WINBIO \_ 擴充 \_ 引擎 \_ 資訊** 結構會套用至指紋辨識器，並在 **專屬** 中包含相關資訊。

</dd> <dt>

**特定**
</dt> <dd>

與特定生物特徵辨識因素相關之生物特徵辨識設備的引擎介面卡功能和註冊需求相關資訊。

<dl> <dt>

**Null**
</dt> <dd>

保留的。 必須為零。

</dd> <dt>

**FacialFeatures**
</dt> <dd>

與臉部特徵相關之生物特徵辨識設備的引擎介面卡功能和註冊需求相關資訊。

<dl> <dt>

**Capabilities**
</dt> <dd>

保留的。 必須為零。

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

保留的。 必須為零。

</dd> </dl> </dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

與指紋模式相關之生物特徵辨識設備的引擎介面卡功能和註冊需求相關資訊。

<dl> <dt>

**Capabilities**
</dt> <dd>

保留的。 必須為零。

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd>

建立新指紋範本所需的良好樣本數。

<dl> <dt>

**GeneralSamples**
</dt> <dd>

建立新指紋範本所需的良好樣本總數。

</dd> <dt>

**中心**
</dt> <dd>

建立新的指紋範本所需之指紋中心的良好樣本數。

</dd> <dt>

**TopEdge**
</dt> <dd>

建立新的指紋範本所需之指紋上邊緣的良好樣本數。

</dd> <dt>

**BottomEdge**
</dt> <dd>

建立新的指紋範本所需之指紋下邊緣的良好樣本數。

</dd> <dt>

**LeftEdge**
</dt> <dd>

建立新的指紋範本所需之指紋左邊緣的良好樣本數。

</dd> <dt>

**RightEdge**
</dt> <dd>

建立新的指紋範本時所需的指紋右邊緣的良好樣本數。

</dd> </dl> </dd> </dl> </dd> <dt>

**虹膜**
</dt> <dd>

與鳶尾花模式相關之生物特徵辨識設備的引擎介面卡功能和註冊需求相關資訊。

<dl> <dt>

**Capabilities**
</dt> <dd>

保留的。 必須為零。

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

保留的。 必須為零。

</dd> </dl> </dd> </dl> </dd> <dt>

**語音**
</dt> <dd>

與語音模式相關的生物特徵辨識單位之引擎介面卡功能和註冊需求的相關資訊。

<dl> <dt>

**Capabilities**
</dt> <dd>

保留的。 必須為零。

</dd> <dt>

**EnrollmentRequirements**
</dt> <dd> <dl> <dt>

**Null**
</dt> <dd>

保留的。 必須為零。

</dd> </dl> </dd> </dl> </dd> </dl> </dd> </dl>

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
</dt> </dl>

 

 





