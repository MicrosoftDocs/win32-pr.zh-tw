---
title: 'DRM_OUTPUT_PROTECTION_EX 結構 (Wmdrmsdk .h) '
description: DRM \_ 輸出 \_ 保護的 \_ EX 結構會保存輸出保護技術的相關資訊。 此結構會藉 \_ \_ 由新增版本號碼來擴充 DRM 輸出保護。
ms.assetid: eeebf5da-172b-4781-8c44-00504a6961bf
keywords:
- DRM_OUTPUT_PROTECTION_EX 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- DRM_OUTPUT_PROTECTION_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeadbb845dc115b1faff858fe3a6ba0064eb425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001188"
---
# <a name="drm_output_protection_ex-structure"></a>DRM \_ 輸出 \_ 保護 \_ EX 結構

**DRM \_ 輸出保護 \_ 的 \_ EX** 結構會保存輸出保護技術的相關資訊。 此結構會藉由新增版本號碼來擴充 **DRM \_ 輸出 \_ 保護** 。

## <a name="syntax"></a>語法


```C++
typedef struct DRM_OUTPUT_PROTECTION_EX {
  DWORD dwVersion;
  GUID  guidId;
  DWORD dwConfigData;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**dwVersion**
</dt> <dd>

版本號碼。

</dd> <dt>

**guidId**
</dt> <dd>

識別輸出保護技術的 GUID。

</dd> <dt>

**dwConfigData**
</dt> <dd>

技術的設定資料。

</dd> </dl>

## <a name="remarks"></a>備註

**DRM \_音訊 \_ 輸出 \_ 保護 \_** （例如和 **drm \_ 影片 \_ 輸出 \_ 保護 \_** ）在 **typedef** 語句中定義為 **DRM \_ 輸出 \_ 保護**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DRM \_ 輸出 \_ 保護**](drm-output-protection.md)
</dt> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





