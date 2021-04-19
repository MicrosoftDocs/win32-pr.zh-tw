---
description: 使用 N 修補程式鑲嵌式配置 Tessellates 指定的網格。
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: 'D3DXTessellateNPatches 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c8811816447deb858b5c8b42d651d219f06fef5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992307"
---
# <a name="d3dxtessellatenpatches-function"></a>D3DXTessellateNPatches 函式

使用 N 修補程式鑲嵌式配置 Tessellates 指定的網格。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMeshIn* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表要 tessellate 的網格。

</dd> <dt>

*pAdjacencyIn* \[在\]
</dt> <dd>

類型： **CONST CONST DWORD \***

指標，指向每個臉部的三個 Dword 陣列，以針對來源網格中的每個臉部指定三個相鄰專案。 這個參數可以是 **Null**。

</dd> <dt>

*NumSegs* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

要 tessellate 的每個邊緣區段數目。

</dd> <dt>

*QuadraticInterpNormals* \[在\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)**

設定為 **TRUE** 以針對法線使用二次插補;線性插補的設定為 **FALSE** 。

</dd> <dt>

*ppMeshOut* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示傳回的鑲嵌網格。

</dd> <dt>

*ppAdjacencyOut* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。 如果這個參數的值不是設定為 **Null**，此緩衝區將會包含每個臉部的三個 dword 陣列，以針對輸出網格中的每個臉部指定三個相鄰專案。 這個參數可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一個值： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

此函式會使用 N 修補演算法 tessellates。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
