---
title: 'WINBIO_BDB_ANSI_381_HEADER 結構 (Winbio \_ 類型 .h) '
description: 指定一系列指紋或棕櫚範例的相關資訊。
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- WINBIO_BDB_ANSI_381_HEADER 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996181"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a>WINBIO \_ BDB \_ ANSI \_ 381 \_ 標頭結構

**WINBIO \_ BDB \_ ANSI \_ 381 \_ 標頭** 結構會指定一系列指紋或棕櫚範例的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a>成員

<dl> <dt>

**RecordLength**
</dt> <dd>

此結構的大小（以位元組為單位），以及從終端使用者所捕獲之指紋或 palm 範例的所有 [**WINBIO \_ BDB \_ ANSI \_ 381 \_ 記錄**](winbio-bdb-ansi-381-record.md) 結構的大小。 只有低6個位元組有效。

</dd> <dt>

**FormatIdentifier**
</dt> <dd>

指定格式。 目前，這必須是0x46495200。

</dd> <dt>

**VersionNumber**
</dt> <dd>

指定版本號碼。 目前，這必須是0x30313000，它會在內部對應至0.1.0.0 版。

</dd> <dt>

**ProductId**
</dt> <dd>

[**WINBIO \_ 註冊的 \_ 格式**](winbio-registered-format.md)結構，其中包含已註冊的資料格式作為擁有者/型別配對。

</dd> <dt>

**CaptureDeviceId**
</dt> <dd>

包含用來捕捉範例之裝置的單位識別碼。

</dd> <dt>

**ImageAcquisitionLevel**
</dt> <dd>

指定要在其中捕獲樣本的解析層級。

</dd> <dt>

**HorizontalScanResolution**
</dt> <dd>

指定掃描的水準解析度。

</dd> <dt>

**VerticalScanResolution**
</dt> <dd>

指定掃描的垂直解析度。

</dd> <dt>

**HorizontalImageResolution**
</dt> <dd>

指定所捕捉的指紋或掌上映射的水準解析度。

</dd> <dt>

**VerticalImageResolution**
</dt> <dd>

指定所捕獲指紋或掌上映射的垂直解析度。

</dd> <dt>

**ElementCount**
</dt> <dd>

此結構中的手指或棕櫚記錄數目。

</dd> <dt>

**ScaleUnits**
</dt> <dd>

包含測量單位，1表示英寸，1表示釐米，2。

</dd> <dt>

**PixelDepth**
</dt> <dd>

指定圖元中的位數。 色彩的每個圖元可以有1到16位。

</dd> <dt>

**ImageCompressionAlg**
</dt> <dd>

指定用來壓縮手指或掌上影像的演算法。

</dd> <dt>

**已保留**
</dt> <dd></dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式結構](client-application-structures.md)
</dt> </dl>

 

 





