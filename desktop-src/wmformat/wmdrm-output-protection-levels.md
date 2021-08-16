---
title: 'WMDRM_OUTPUT_PROTECTION_LEVELS 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 輸出 \_ 保護 \_ 層級結構包含 (OPLs) 的輸出保護層級，以執行各種動作的授權所需。
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- WMDRM_OUTPUT_PROTECTION_LEVELS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a19d7098266857f8a17e395ad749b216e45ce101278812f67c032943933955a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843959"
---
# <a name="wmdrm_output_protection_levels-structure"></a>WMDRM \_ 輸出 \_ 保護 \_ 層級結構

**WMDRM \_ 輸出 \_ 保護 \_ 層級** 結構包含 (OPLs) 的輸出保護層級，以執行各種動作的授權所需。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**wCompressedDigitalVideo**
</dt> <dd>

接收壓縮數位影片所需的最小 OPL。

</dd> <dt>

**wUncompressedDigitalVideo**
</dt> <dd>

接收未壓縮數位影片所需的最小 OPL。

</dd> <dt>

**wAnalogVideo**
</dt> <dd>

接收類比影片所需的最小 OPL。

</dd> <dt>

**wCompressedDigitalAudio**
</dt> <dd>

接收壓縮數位音訊所需的最小 OPL。

</dd> <dt>

**wUncompressedDigitalAudio**
</dt> <dd>

接收未壓縮數位音訊所需的最小 OPL。

</dd> <dt>

**wMinimumCopyProtectionLevel**
</dt> <dd>

複製內容所需的最小 OPL。

</dd> </dl>

## <a name="remarks"></a>備註

此結構是由 [**IWMDRMLicense：： GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) 方法所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





