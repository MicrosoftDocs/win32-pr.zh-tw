---
description: 描述 JPEG AC huffman 資料表。
ms.assetid: E1923FFA-E7E5-4158-9793-3E7F5A6EA7FA
title: 'DXGI_JPEG_AC_HUFFMAN_TABLE 結構 (Dxgitype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXGI_JPEG_AC_HUFFMAN_TABLE
api_type:
- HeaderDef
api_location:
- dxgitype.h
ms.openlocfilehash: 21e279e4974d221a6feba6f135343d122f30f3da1edb18210e0e14f92fdb94a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518371"
---
# <a name="dxgi_jpeg_ac_huffman_table-structure"></a>DXGI \_ JPEG \_ AC \_ HUFFMAN \_ 資料表結構

描述 JPEG AC huffman 資料表。

## <a name="syntax"></a>語法


```C++
typedef struct DXGI_JPEG_AC_HUFFMAN_TABLE {
  BYTE CodeCounts[16];
  BYTE CodeValues[162];
} DXGI_JPEG_AC_HUFFMAN_TABLE;
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

 

 




