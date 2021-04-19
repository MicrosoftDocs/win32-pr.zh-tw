---
description: 為三角形清單產生優化的頂點對應。 在套用 D3DXOptimizeFaces 所產生的臉部重新對應之後，通常會使用此函數。
ms.assetid: a3b9cb68-204e-4e8f-a985-738d1cea1e29
title: 'D3DXOptimizeVertices 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 734c2224ae29e7ab166010d59859d00355e5400e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992291"
---
# <a name="d3dxoptimizevertices-function"></a>D3DXOptimizeVertices 函式

為三角形清單產生優化的頂點對應。 在套用 [**D3DXOptimizeFaces**](d3dxoptimizefaces.md)所產生的臉部重新對應之後，通常會使用此函數。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXOptimizeVertices(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pVertexRemap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pIndices* \[在\]
</dt> <dd>

類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**

用來排序頂點的三角形清單索引指標。

</dd> <dt>

*NumFaces* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

三角形清單中的臉部數目。

</dd> <dt>

*NumVertices* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

三角形清單所參考的頂點數目。

</dd> <dt>

*Indices32Bit* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

表示索引類型的旗標：如果索引是32位 (超過65535個頂點) ，則為 **TRUE** ，如果索引為16位 (65535 或較少的頂點) ，則為 **FALSE** 。

</dd> <dt>

*pVertexRemap* \[in、out\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

目的地緩衝區的指標，其中將包含每個頂點的新索引。 針對指定專案儲存在 *pVertexRemap* 中的值是新頂點順序中的來源頂點位置。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

依預設，網格會在建立時使用16位索引，除非應用程式另有指定。 若要檢查現有的網狀架構是否使用16位或32位的索引，請呼叫 [**ID3DXBaseMesh：： GetOptions**](id3dxbasemesh--getoptions.md) ，並檢查 D3DXMESH 的 \_ 32 位旗標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
