---
title: 'WMDRM_ENCRYPT_SCATTER_BLOCK 結構 (Wmdrmsdk .h) '
description: WMDRM \_ 加密 \_ 散佈 \_ 區塊結構包含要加密的資料區塊。
ms.assetid: 73c871f0-3d0d-480f-856c-0f7d5dde5895
keywords:
- WMDRM_ENCRYPT_SCATTER_BLOCK 結構 windows 媒體格式
- 結構 windows 媒體格式
topic_type:
- apiref
api_name:
- WMDRM_ENCRYPT_SCATTER_BLOCK
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 258cb7e0d8d2cac8da40197aaa45028a56af0ff3a313d65c1a98c50d45b8d3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119658158"
---
# <a name="wmdrm_encrypt_scatter_block-structure"></a>WMDRM \_ 加密 \_ 散佈 \_ 區塊結構

**WMDRM \_ 加密 \_ 散佈 \_ 區塊** 結構包含要加密的資料區塊。

## <a name="syntax"></a>語法


```C++
typedef struct WMDRM_ENCRYPT_SCATTER_BLOCK {
  DWORD dwStreamID;
  DWORD cbBlock;
  BYTE  *pbBlock;
} ;
```



## <a name="members"></a>成員

<dl> <dt>

**dwStreamID**
</dt> <dd>

資料區塊所屬資料流程的識別碼。

</dd> <dt>

**cbBlock**
</dt> <dd>

區塊的大小（以位元組為單位）。

</dd> <dt>

**pbBlock**
</dt> <dd>

包含資料區塊之緩衝區的指標。

</dd> </dl>

## <a name="remarks"></a>備註

[**IWMDRMEncryptScatter：： EncryptScatter**](iwmdrmencryptscatter-encryptscatter.md)方法會使用此結構來識別要加密的資料區塊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構**](drm-structures.md)
</dt> </dl>

 

 





