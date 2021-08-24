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
ms.openlocfilehash: d2ec6e376b2df4cd3e5462766d6fd992ed7d2356a1bc81d0ff74c662a99697af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708978"
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

 

 





