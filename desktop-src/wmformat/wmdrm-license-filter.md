---
title: 'WMDRM_LICENSE_FILTER 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 授權 \_ 篩選結構會定義要在建立授權列舉時使用的篩選參數。
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- WMDRM_LICENSE_FILTER 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94dc65758c7c5a25d31dd9fdb2d0fcd5cfa65debfff3defab4b88280a5ff3b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698135"
---
# <a name="wmdrm_license_filter-structure"></a>WMDRM \_ 授權 \_ 篩選結構

**WMDRM \_ 授權 \_ 篩選** 結構會定義要在建立授權列舉時使用的篩選參數。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**dwVersion**
</dt> <dd>

指定所傳回授權的最小版本號碼。

</dd> <dt>

**bstrKID**
</dt> <dd>

指定用來篩選授權的金鑰識別碼。 列舉中只會包含具有指定金鑰識別碼的授權。

</dd> <dt>

**bstrRights**
</dt> <dd>

指定要篩選授權的一組許可權。 列舉中只會包含提供所有指定許可權的授權。

</dd> <dt>

**bstrAllowedSourceIDs**
</dt> <dd>

指定要包含在授權搜尋中的受保護內容來源。

</dd> </dl>

## <a name="remarks"></a>備註

此結構是由 [**IWMDRMLicenseManagement：： CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md) 方法所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





