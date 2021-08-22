---
title: 'WMDRM_ENCRYPT_SCATTER_INFO 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 加密 \_ 散佈 \_ 資訊結構包含設定 IWMDRMEncryptScatter 介面以供使用所需的資訊。
ms.assetid: 25e19511-56ac-441b-b521-5097dd792ead
keywords:
- WMDRM_ENCRYPT_SCATTER_INFO 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_INFO
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef766f40742713b01648348bedb4c1a35494fdc02d02843f8f2a41f133938a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083812"
---
# <a name="wmdrm_encrypt_scatter_info-structure"></a>WMDRM \_ 加密 \_ 散佈 \_ 資訊結構

**WMDRM \_ 加密 \_ 散佈 \_ 資訊** 結構包含設定 [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)介面以供使用所需的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_INFO {
  DWORD dwStreamID;
  DWORD dwSampleProtectionVersion;
  DWORD cbProtectionInfo;
  BYTE  *pbProtectionInfo;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**dwStreamID**
</dt> <dd>

要加密之資料流程的識別碼。

</dd> <dt>

**dwSampleProtectionVersion**
</dt> <dd>

用來從指定的資料流程編碼資料的範例保護版本。

</dd> <dt>

**cbProtectionInfo**
</dt> <dd>

**PbProtectionInfo** 緩衝區的大小（以位元組為單位）。

</dd> <dt>

**pbProtectionInfo**
</dt> <dd>

包含額外保護資訊的緩衝區。

</dd> </dl>

## <a name="remarks"></a>備註

此結構是由 [**IWMDRMEncryptScatter：： InitEncryptScatter**](iwmdrmencryptscatter-initencryptscatter.md) 方法所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





