---
title: 'DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS 結構 (Wmdrmsdk .h) '
description: DRM 的 \_ 最小 \_ 輸出 \_ 保護 \_ 層級結構會保有最小輸出保護層級 (OPLs) 來播放各種類型的內容。 裝置必須支援一種資料類型的最小 OPL，才能從讀取器接收該類型的資料。
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5559527507f0399a09661dfe380f51d11e10750eddf7d996b38d110e4f38e37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708918"
---
# <a name="drm_minimum_output_protection_levels-structure"></a>DRM \_ 最小 \_ 輸出 \_ 保護 \_ 層級結構

**DRM 的 \_ 最小 \_ 輸出 \_ 保護 \_ 層級** 結構會保有最小輸出保護層級 (OPLs) 來播放各種類型的內容。 裝置必須支援一種資料類型的最小 OPL，才能從讀取器接收該類型的資料。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
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

</dd> </dl>

## <a name="remarks"></a>備註

此結構會當做 [**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md) 結構的成員使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





