---
title: 'WINBIO_EXTENDED_STORAGE_INFO 結構 (Winbio \_ 類型 .h) '
description: 包含生物識別設備之儲存體介面卡的功能和註冊需求相關資訊。
ms.assetid: 7A648610-E947-4967-A9AF-C8A9C0B81D92
keywords:
- WINBIO_EXTENDED_STORAGE_INFO 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EXTENDED_STORAGE_INFO 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_STORAGE_INFO
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e8a9f133baf77a77d3db33001e996accc9574f86ad708037900a5db7c0c5e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910379"
---
# <a name="winbio_extended_storage_info-structure"></a>WINBIO \_ 延伸 \_ 儲存體 \_ 資訊結構

包含生物識別設備之儲存體介面卡的功能和註冊需求相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_EXTENDED_STORAGE_INFO {
  WINBIO_CAPABILITIES   GenericStorageCapabilities;
  WINBIO_BIOMETRIC_TYPE Factor;
  union {
    ULONG32 Null;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } FacialFeatures;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Fingerprint;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Iris;
    struct {
      WINBIO_CAPABILITIES Capabilities;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_STORAGE_INFO, *PWINBIO_EXTENDED_STORAGE_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**GenericStorageCapabilities**
</dt> <dd>

連接到特定生物識別單位之儲存體元件的一般功能。

</dd> <dt>

**因素**
</dt> <dd>

此結構包含存放裝置介面卡功能和註冊需求相關資訊的生物特徵辨識單位類型。 例如，如果 **因素** 成員的值是 **WINBIO \_ 類型 \_ 指紋**， **WINBIO \_ 延伸 \_ 儲存體 \_ 資訊** 結構會套用至指紋辨識器，並在 **專屬** 中包含相關資訊。

</dd> <dt>

**特定**
</dt> <dd>

與特定生物特徵辨識因素相關之生物特徵辨識設備的存放裝置介面卡功能和註冊需求相關資訊。

<dl> <dt>

**Null**
</dt> <dd>

保留的。 必須為零。

</dd> <dt>

**FacialFeatures**
</dt> <dd>

與臉部特徵相關的生物特徵辨識設備之存放裝置介面卡的功能和註冊需求相關資訊。

<dl> <dt>

**Capabilities**
</dt> <dd>

連接到特定生物特徵辨識裝置的儲存元件臉部辨識功能。

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

與指紋模式相關之生物特徵辨識設備的儲存介面卡功能和註冊需求相關資訊。

<dl> <dt>

**Capabilities**
</dt> <dd>

連線到特定生物識別單位之儲存體元件的指紋辨識功能

</dd> </dl> </dd> <dt>

**虹膜**
</dt> <dd>

與鳶尾花模式相關的生物特徵辨識單位之儲存體介面卡的功能和註冊需求相關資訊。

<dl> <dt>

**Capabilities**
</dt> <dd>

連線到特定生物識別單位之儲存體元件的鳶尾花辨識功能

</dd> </dl> </dd> <dt>

**語音**
</dt> <dd>

與語音模式相關的生物特徵辨識單位之存放裝置介面卡的功能和註冊需求相關資訊。

<dl> <dt>

**Capabilities**
</dt> <dd>

連線到特定生物識別單位之儲存體元件的語音辨識功能

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WINBIO \_ 生物特徵辨識 \_ 類型常數**](winbio-biometric-type-constants.md)
</dt> <dt>

[**WINBIO \_ 功能常數**](winbio-capability-constants.md)
</dt> </dl>

 

 





