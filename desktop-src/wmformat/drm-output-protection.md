---
title: 'DRM_OUTPUT_PROTECTION 結構 (Wmdrmsdk .h) '
description: DRM \_ 輸出 \_ 保護結構會保存輸出保護技術的相關資訊。
ms.assetid: e458013d-b77e-4e03-bff9-e3ecfc72ebdb
keywords:
- DRM_OUTPUT_PROTECTION 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a10428d86503e952dc82a7d45bddc11f5dd1286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978748"
---
# <a name="drm_output_protection-structure"></a>DRM \_ 輸出 \_ 保護結構

**DRM \_ 輸出 \_ 保護** 結構會保存輸出保護技術的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_OUTPUT_PROTECTION {
  GUID guidId;
  BYTE bConfigData;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**guidId**
</dt> <dd>

識別輸出保護技術的 GUID。

</dd> <dt>

**bConfigData**
</dt> <dd>

技術的設定資料。

</dd> </dl>

## <a name="remarks"></a>備註

**DRM \_音訊 \_ 輸出 \_ 保護** 和 **drm \_ 影片 \_ 輸出 \_ 保護** 都會定義為 **typedef** 語句中的 **DRM \_ 輸出 \_ 保護**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM \_ 輸出 \_ 保護， \_ 例如**](drm-output-protection-ex.md)
</dt> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





