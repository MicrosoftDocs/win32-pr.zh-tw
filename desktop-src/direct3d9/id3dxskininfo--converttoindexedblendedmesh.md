---
description: 使用網格，並傳回具有個別頂點 blend 加權、索引和骨骼組合表的新網格。 表格描述哪些骨骼調色板會影響網格的哪些子集。
ms.assetid: e4758a3b-8a45-4ed3-aa62-9713d12afc56
title: 'ID3DXSkinInfo：： ConvertToIndexedBlendedMesh 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.ConvertToIndexedBlendedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9aa2b4bef607197c0f6fea084054d0e4fed1c721388677d45b465aff9c39ce49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790448"
---
# <a name="id3dxskininfoconverttoindexedblendedmesh-method"></a>ID3DXSkinInfo：： ConvertToIndexedBlendedMesh 方法

使用網格，並傳回具有個別頂點 blend 加權、索引和骨骼組合表的新網格。 表格描述哪些骨骼調色板會影響網格的哪些子集。

## <a name="syntax"></a>語法


```C++
HRESULT ConvertToIndexedBlendedMesh(
  [in]        LPD3DXMESH   pMesh,
  [in]        DWORD        Options,
  [in]        DWORD        paletteSize,
  [in]  const DWORD        *pAdjacencyIn,
  [in]        LPDWORD      pAdjacencyOut,
  [out]       DWORD        *pFaceRemap,
  [out]       LPD3DXBUFFER *ppVertexRemap,
  [out]       DWORD        *pMaxVertexInfl,
  [out]       DWORD        *pNumBoneCombinations,
  [out]       LPD3DXBUFFER *ppBoneCombinationTable,
  [out]       LPD3DXMESH   *ppMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

輸入網格。 請參閱 [**ID3DXMesh**](id3dxmesh.md)。

</dd> <dt>

*選項* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

目前未使用。

</dd> <dt>

*paletteSize* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

適用于矩陣調色板外觀的骨骼矩陣數目。

</dd> <dt>

*pAdjacencyIn* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

輸入網格相鄰資訊。

</dd> <dt>

*pAdjacencyOut* \[在\]
</dt> <dd>

類型： **[ **LPDWORD**](../winprog/windows-data-types.md)**

輸出網格相鄰資訊。

</dd> <dt>

*pFaceRemap* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

Dword 的陣列，每個臉部各一個，用來識別對應至混合網格中各臉部的原始網格臉部。 如果提供給此引數的值為 **Null**，則不會傳回臉部重新對應資料。

</dd> <dt>

*ppVertexRemap* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含每個頂點的 DWORD，以指定新頂點如何對應至舊頂點。 如果您需要根據新的頂點對應來改變外部資料，這個重新對應會很有用。 這個參數是選擇性的;可以使用 **Null** 。

</dd> <dt>

*pMaxVertexInfl* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

DWORD 的指標，其中將包含此外觀方法的每個頂點所需的最大骨骼數目。

</dd> <dt>

*pNumBoneCombinations* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

骨骼組合表中的骨骼數目指標。

</dd> <dt>

*ppBoneCombinationTable* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

骨骼組合表的指標。 資料會組織成 [**D3DXBONECOMBINATION**](d3dxbonecombination.md) 結構。

</dd> <dt>

*ppMesh* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

新網格的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果方法成功，則傳回值為「D3D \_ 正常」。 如果方法失敗，則傳回值可以是 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

重新對應陣列中的每個專案都會指定該位置的前一個索引。 例如，如果頂點位於位置3，但已重新對應到位置5，則 pVertexRemap 的第五個元素將包含3個。

這個方法不會在不支援固定函式頂點混合的硬體上執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
