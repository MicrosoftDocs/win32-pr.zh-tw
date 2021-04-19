---
description: 描述 JPEG 量化資料表。
ms.assetid: DE1AAB15-B0B8-4594-BBCE-5F8EE5CE0AF7
title: 'DXGI_JPEG_QUANTIZATION_TABLE 結構 (Dxgitype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_QUANTIZATION_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 2b0a097cb4c364ecc14e471f7c15f642aa65e912
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985878"
---
# <a name="dxgi_jpeg_quantization_table-structure"></a>DXGI \_ JPEG \_ 量化 \_ 資料表結構

描述 JPEG 量化資料表。

## <a name="syntax"></a>語法


```C++
typedef struct DXGI_JPEG_QUANTIZATION_TABLE {
  BYTE Elements[64];
} DXGI_JPEG_QUANTIZATION_TABLE;
```



## <a name="members"></a>成員

<dl> <dt>

**元素**
</dt> <dd>

包含量化資料表元素的位元組陣列。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dxgitype。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DXGI 結構](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




