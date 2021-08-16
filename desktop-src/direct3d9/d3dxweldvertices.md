---
description: 將具有相同屬性的已複寫頂點一起進行焊縫。 這個方法會使用指定的 epsilon 值進行相等比較。
ms.assetid: bddf6e0c-55a1-40d2-8681-e7f0f9002bfa
title: 'D3DXWeldVertices 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXWeldVertices
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3ce6a9a05573467e0725785a6272e5542c4f871080fe221ac12078b17165eb5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118803271"
---
# <a name="d3dxweldvertices-function"></a>D3DXWeldVertices 函式

將具有相同屬性的已複寫頂點一起進行焊縫。 這個方法會使用指定的 epsilon 值進行相等比較。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXWeldVertices(
  _In_          LPD3DXMESH       pMesh,
  _In_          DWORD            Flags,
  _In_    const D3DXWeldEpsilons *pEpsilons,
  _In_    const DWORD            *pAdjacencyIn,
  _Inout_       DWORD            *pAdjacencyOut,
  _Out_         DWORD            *pFaceRemap,
  _Out_         LPD3DXBUFFER     *ppVertexRemap
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

[**ID3DXMesh**](id3dxmesh.md)物件的指標，也就是用來焊接頂點的網格。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

[**D3DXWELDEPSILONSFLAGS**](./d3dxweldepsilonsflags.md)中一或多個旗標的組合。

</dd> <dt>

*pEpsilons* \[在\]
</dt> <dd>

Type： **Const [**D3DXWeldEpsilons**](d3dxweldepsilons.md) \***

[**D3DXWeldEpsilons**](d3dxweldepsilons.md)結構的指標，指定要用於此方法的 epsilon 值。 使用 **Null** 將所有結構成員初始化為預設值 1.0 e-6f。

</dd> <dt>

*pAdjacencyIn* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，以針對來源網格中的每個臉部指定三個相鄰專案。 如果邊緣沒有連續的臉部，則值為0xffffffff。 如果此參數設定為 **Null**，則會呼叫 [**ID3DXBaseMesh：： GenerateAdjacency**](id3dxbasemesh--generateadjacency.md) 來建立邏輯相鄰資訊。

</dd> <dt>

*pAdjacencyOut* \[in、out\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

指標，指向每個臉部的三個 Dword 陣列，以針對優化網格中的每個臉部指定三個相鄰專案。 如果邊緣沒有連續的臉部，則值為0xffffffff。

</dd> <dt>

*pFaceRemap* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

Dword 的陣列，每個臉部各一個，用來識別對應至焊接網格中各臉部的原始網格臉部。

</dd> <dt>

*ppVertexRemap* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址，其中包含每個頂點的 DWORD，以指定新頂點如何對應至舊頂點。 如果您需要根據新的頂點對應來改變外部資料，這個重新對應會很有用。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

此函數會使用提供的相鄰資訊來判斷複寫的點。 頂點會根據 epsilon 比較來合併。 具有相等位置的頂點必須已經過計算，並以點代表資料表示。

此函式會結合具有類似元件的邏輯上焊接頂點，例如 pEpsilons 內的法線或紋理座標。

下列範例程式碼會呼叫此函數，並啟用焊接。 頂點會使用標準向量和頂點位置的 epsilon 值進行比較。 指標會傳回至臉部重新對應陣列， (*pFaceRemap*) 。


```
TCHAR            strMediaPath[512];       // X-file path 
LPD3DXBUFFER     pAdjacencyBuffer = NULL; // adjacency data buffer
LPD3DXBUFFER     pD3DXMtrlBuffer  = NULL; // material buffer
LPD3DXMESH       pMesh            = NULL; // mesh object
DWORD            m_dwNumMaterials;        // number of materials
D3DXWELDEPSILONS Epsilons;                // structure with epsilon values
DWORD            *pFaceRemap[65536];      // face remapping array
DWORD            i;                       // internal variable
    
    // Load the mesh from the specified file
    hr = D3DXLoadMeshFromX ( strMediaPath,
                         D3DXMESH_MANAGED,
                         m_pd3dDevice,
                         &pAdjacencyBuffer,
                         &pD3DXMtrlBuffer,
                         NULL,
                         &m_dwNumMaterials,
                         &pMesh ) )
                             
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
    
    // Set epsilon values
    Epsilons.Normal = 0.001;
    Epsilons.Position = 0.1;
    
    // Weld the vertices
    for( i=0; i < 65536; i++ )
    { 
        pFaceRemap[i] = 0; 
    }
    
    hr = D3DXWeldVertices ( pMesh,
                            D3DXWELDEPSILONS_WELDPARTIALMATCHES,
                            &Epsilons,
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pAdjacencyBuffer->GetBufferPointer(),
                            (DWORD*)pFaceRemap,
                            NULL )
                            
    if( FAILED( hr ) ) 
      goto End;              // Go to error handling
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
