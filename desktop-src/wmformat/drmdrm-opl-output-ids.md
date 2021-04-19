---
title: 'DRM_OPL_OUTPUT_IDS 結構 (Wmdrmsdk .h) '
description: DRM \_ OPL \_ 輸出 \_ 識別碼結構會保存多個輸出保護層級 (OPL) 輸出識別碼。
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- DRM_OPL_OUTPUT_IDS 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983114"
---
# <a name="drm_opl_output_ids-structure"></a>DRM \_ OPL \_ 輸出 \_ 識別碼結構

**DRM \_ OPL \_ 輸出 \_** 識別碼結構會保存多個輸出保護層級 (OPL) 輸出識別碼。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**Cid**
</dt> <dd>

**RgIds** 所參考之陣列中的識別碼數目。

</dd> <dt>

**rgIds**
</dt> <dd>

Guid 陣列的位址。 陣列的每個成員都包含 OPL 輸出識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

此結構會當做 [**drm \_ 複製 \_ OPL**](drmdrm-copy-opl.md) 和 [**drm \_ PLAY \_ OPL**](drmdrm-play-opl.md) 結構的成員使用，以識別輸出識別碼的群組。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





