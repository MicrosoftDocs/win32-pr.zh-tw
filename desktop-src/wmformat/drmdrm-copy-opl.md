---
title: 'DRM_COPY_OPL 結構 (Wmdrmsdk .h) '
description: DRM \_ 複製 \_ OPL 結構會保存輸出保護層級的相關資訊， (OPLs 在複製動作的授權中指定的) 。
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- DRM_COPY_OPL 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980146"
---
# <a name="drm_copy_opl-structure"></a>DRM \_ 複製 \_ OPL 結構

**DRM \_ 複製 \_ OPL** 結構會保存輸出保護層級的相關資訊， (OPLs 在複製動作的授權中指定的) 。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**wMinimumCopyLevel**
</dt> <dd>

複製動作的最小 OPL。

</dd> <dt>

**oplIdIncludes**
</dt> <dd>

[**DRM \_OPL \_ 輸出 \_**](drmdrm-opl-output-ids.md) 識別碼結構，其中包含要允許的技術識別碼。 此成員用於指派的 OPLs 低於最小複製層級的輸出技術，但可將內容複寫到其中。

</dd> <dt>

**oplIdExcludes**
</dt> <dd>

[**DRM \_OPL \_ 輸出 \_**](drmdrm-opl-output-ids.md) 識別碼結構，其中包含要限制之技術的輸出識別碼。 此成員用於指派的 OPLs 超過最小複製層級的輸出技術，但授權簽發者不會授與複製的許可權。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM \_ PLAY \_ OPL**](drmdrm-play-opl.md)
</dt> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





