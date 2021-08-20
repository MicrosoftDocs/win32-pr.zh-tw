---
description: 包含記憶體壓力報告的資料。
ms.assetid: bdf65d35-281f-4795-a2c1-0d4e91bfa7bc
title: 'D3DMEMORYPRESSURE 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMEMORYPRESSURE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: ca5a6dd95a35cae231b80fbeee9ee05bbdfe9f0ecacc70b13493ad8d16739637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911092"
---
# <a name="d3dmemorypressure-structure-d3d9typesh"></a>D3DMEMORYPRESSURE 結構 (D3d9types .h) 

包含記憶體壓力報告的資料。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DMEMORYPRESSURE {
  UINT64 BytesEvictedFromProcess;
  UINT64 SizeOfInefficientAllocation;
  DWORD  LevelOfEfficiency;
} D3DMEMORYPRESSURE;
```



## <a name="members"></a>成員

<dl> <dt>

**BytesEvictedFromProcess**
</dt> <dd>

類型： **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

進程在查詢期間收回的位元組數目。

</dd> <dt>

**SizeOfInefficientAllocation**
</dt> <dd>

類型： **[ **UINT64**](../winprog/windows-data-types.md)**

</dd> <dd>

因為慣用記憶體區段內的空間不足，所以放置在非最非最非最佳記憶體區段中的位元組總數。

</dd> <dt>

**LevelOfEfficiency**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

放在非最佳記憶體中之記憶體配置的整體效率。 此值以百分比表示。 例如，值95表示放置在 nonpreferred 記憶體區段中的配置為95% 的效率。 此數位不應視為確切的度量。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
