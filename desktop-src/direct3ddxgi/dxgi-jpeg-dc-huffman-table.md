---
description: 描述 JPEG DC huffman 資料表。
ms.assetid: 9D6C18C3-F75C-41E0-9EFA-E882E89DE713
title: 'DXGI_JPEG_DC_HUFFMAN_TABLE 結構 (Dxgitype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_DC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: b2f5f73f7c6def745b987818b9ec30fb3e2752e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196231"
---
# <a name="dxgi_jpeg_dc_huffman_table-structure"></a>DXGI \_ JPEG \_ DC \_ HUFFMAN \_ 資料表結構

描述 JPEG DC huffman 資料表。

## <a name="syntax"></a>語法


```C++
typedef struct DXGI_JPEG_DC_HUFFMAN_TABLE {
  BYTE CodeCounts[12];
  BYTE CodeValues[12];
} DXGI_JPEG_DC_HUFFMAN_TABLE;
```



## <a name="members"></a>成員

<dl> <dt>

**CodeCounts**
</dt> <dd>

每個程式碼長度的程式碼數目。

</dd> <dt>

**CodeValues**
</dt> <dd>

Huffman 代碼值，以增加程式碼長度的順序排列。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dxgitype。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DXGI 結構](d3d10-graphics-reference-dxgi-structures.md)
</dt> </dl>

 

 




