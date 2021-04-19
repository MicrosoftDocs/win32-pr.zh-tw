---
description: 使用提供的加權（盡可能接近指定的 MinValue）產生簡化的網格。
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: 'D3DXSimplifyMesh 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0258047631a41e31d108ba45531988e4cb6a35ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993878"
---
# <a name="d3dxsimplifymesh-function"></a>D3DXSimplifyMesh 函式

使用提供的加權（盡可能接近指定的 MinValue）產生簡化的網格。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

[**ID3DXMesh**](id3dxmesh.md)介面的指標，代表來源網格。

</dd> <dt>

*pAdjacency* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，以指定要簡化網格中每個臉部的三個相鄰專案。

</dd> <dt>

*pVertexAttributeWeights* \[在\]
</dt> <dd>

Type： **Const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***

[**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md)結構的指標，其中包含每個頂點元件的權數。 如果此參數設定為 **Null**，則會使用預設結構。 請參閱＜備註＞。

</dd> <dt>

*pVertexWeights* \[在\]
</dt> <dd>

Type： **Const [**FLOAT**](../winprog/windows-data-types.md) \***

頂點加權陣列的指標。 如果此參數設定為 **Null**，則所有頂點加權都會設定為1.0。

</dd> <dt>

*MinValue* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

頂點或臉部的數目（視 *Options* 參數中設定的旗標而定），藉此簡化來源網格。

</dd> <dt>

*選項* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

指定網格的簡化選項。 您可以設定 [**D3DXMESHSIMP**](./d3dxmeshsimp.md) 中的其中一個旗標。

</dd> <dt>

*ppMesh* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

[**ID3DXMesh**](id3dxmesh.md)介面指標的位址，表示傳回的簡化網格。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

此函數會產生具有 *MinValue* 頂點或臉部的網格。

如果簡化程式無法減少 *MinValue* 的網格，則呼叫仍然會成功，因為 *MinValue* 是所需的最小值，而不是絕對最小值。

如果 *pVertexAttributeWeights* 設定為 **Null**，則會將下列值指派給預設的 [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) 結構。


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



這是大部分應用程式應該使用的預設結構，因為它只會考慮幾何和一般調整。 只有在特殊情況下，才會需要修改其他成員欄位。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
