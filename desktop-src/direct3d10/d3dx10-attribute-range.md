---
description: 儲存屬性資料表專案。
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: 'D3DX10_ATTRIBUTE_RANGE 結構 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ddf7f10882e08232467130b3abbc6fb723a843ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992343"
---
# <a name="d3dx10_attribute_range-structure"></a>D3DX10 \_ 屬性 \_ 範圍結構

儲存屬性資料表專案。

## <a name="syntax"></a>語法


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a>成員

<dl> <dt>

**AttribId**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

屬性資料表識別碼。

</dd> <dt>

**FaceStart**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

開始臉部。

</dd> <dt>

**FaceCount**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

臉部計數。

</dd> <dt>

**VertexStart**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

正在啟動頂點。

</dd> <dt>

**VertexCount**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

頂點計數。

</dd> </dl>

## <a name="remarks"></a>備註

屬性工作表用來識別需要以不同紋理、轉譯狀態、材質等等繪製的網格區域。 此外，應用程式也可以使用屬性工作表來隱藏部分網格，而不是在繪製框架時 (AttribId) 繪製指定的屬性識別碼。

LPD3DX \_ 屬性 \_ 範圍類型定義為 D3DX \_ 屬性 \_ 範圍結構的指標。


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3DX10。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
