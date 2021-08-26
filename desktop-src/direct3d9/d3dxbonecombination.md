---
description: 描述具有相同屬性和骨骼組合的網格子集。
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: 'D3DXBONECOMBINATION 結構 (D3dx9mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 72d60b5c87d43763be4700ba7931c61c41cf0101d80390afb737c7f4afda83a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952488"
---
# <a name="d3dxbonecombination-structure"></a>D3DXBONECOMBINATION 結構

描述具有相同屬性和骨骼組合的網格子集。

## <a name="syntax"></a>語法


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a>成員

<dl> <dt>

**AttribId**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

屬性資料表識別碼。

</dd> <dt>

**FaceStart**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

開始臉部。

</dd> <dt>

**FaceCount**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

臉部計數。

</dd> <dt>

**VertexStart**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

正在啟動頂點。

</dd> <dt>

**VertexCount**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

頂點計數。

</dd> <dt>

**BoneId**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

</dd> <dd>

值陣列的指標，可識別可在單一繪圖呼叫中繪製的每個骨骼。 請注意，陣列的長度可以是可變長度，以容納 [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)的可變長度骨骼組合。

陣列的大小會根據所產生的網狀架構類型而有所不同。 非索引的網狀陣列大小等於 [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)) 中每個頂點 (pMaxVertexInfl 的加權數目。 索引的網狀陣列大小等於 [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)) 中 (paletteSize 的骨骼矩陣調色板專案數目。

</dd> </dl>

## <a name="remarks"></a>備註

**D3DXBONECOMBINATION** 所描述之網格的子集可以在單一繪圖呼叫中轉譯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3dx9mesh。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 結構](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
