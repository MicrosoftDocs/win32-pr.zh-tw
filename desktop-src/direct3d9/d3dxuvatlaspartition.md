---
description: D3DXUVAtlasPartition 函式-建立網格的 UV 塔。
ms.assetid: c46f3e47-8e72-435c-875d-cccfa4b893a2
title: 'D3DXUVAtlasPartition 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPartition
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 63df6bbcc1b811b9617796bc6e7e51af2dfdca56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117796"
---
# <a name="d3dxuvatlaspartition-function"></a>D3DXUVAtlasPartition 函式

建立網格的 UV 塔。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXUVAtlasPartition(
  _In_        LPD3DXMESH      pMesh,
  _In_        UINT            dwMaxChartNumber,
  _In_        FLOAT           fMaxStretch,
  _In_        DWORD           dwTextureIndex,
  _In_  const DWORD           *pdwAdjacency,
        const DWORD           *pdwFalseEdges,
  _In_        FLOAT           *pfIMTArray,
  _In_        LPD3DXUVATLASCB pCallback,
  _In_        FLOAT           fCallbackFrequency,
  _In_        LPVOID          pUserContent,
  _In_        DWORD           dwOptions,
  _In_        LPD3DXMESH      *ppMeshOut,
  _Out_       LPD3DXBUFFER    pFacePartitioning,
  _Out_       LPD3DXBUFFER    *ppVertexRemapArray,
              LPD3DXBUFFER    *ppPartitionResultAdjacency,
  _Out_       FLOAT           *pfMaxStretchOut,
  _Out_       UINT            *pdwNumChartsOut
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算塔的物件幾何。 網格至少必須包含位置資料和2D 材質座標。

</dd> <dt>

*dwMaxChartNumber* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

要分割網格的圖表數目上限。 請參閱有關資料分割模式的備註。 使用0可告訴 D3DX，應該根據 stretch 將塔參數化。

</dd> <dt>

*fMaxStretch* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

允許的延展量。 0表示不允許延展，1表示可以使用任何數量的延展。

</dd> <dt>

*dwTextureIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

以零為基礎的材質座標索引，識別要使用的材質座標集。

</dd> <dt>

*pdwAdjacency* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

相鄰資料陣列的指標，每個臉部有3個 Dword，指出哪些三角形彼此相鄰 (請參閱 [**ID3DXBaseMesh：： GenerateAdjacency**](id3dxbasemesh--generateadjacency.md)) 。

</dd> <dt>

*pdwFalseEdges* 
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

每個臉部有3個 DWORD 的陣列。 每個臉部都會指出邊緣是否為 false。 非 false 的邊緣會以-1 表示，錯誤的邊緣會以任何其他值表示。 這會啟用四邊形網格的參數化，其中每個四條中間的邊緣將不會被剪下。

</dd> <dt>

*pfIMTArray* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

整合式計量張量陣列的指標，描述如何延展三角形 (查看 [IntegratedMetricTensor](using-uvatlas.md)) 。

</dd> <dt>

*pCallback* \[在\]
</dt> <dd>

類型： **[LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)**

回呼函式的指標 (查看適用于監視進度的 [LPD3DXU加值稅LASCB](lpd3dxuvatlascb.md)) 。

</dd> <dt>

*fCallbackFrequency* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

指定 D3DX 將呼叫回呼的頻率;合理的預設值是 0.0001 f。

</dd> <dt>

*pUserContent* \[在\]
</dt> <dd>

類型： **[ **LPVOID**](../winprog/windows-data-types.md)**

傳遞給回呼函式的使用者定義值指標。通常由應用程式用來傳遞資料結構的指標，以提供回呼函數的內容資訊。

</dd> <dt>

*>dwoptions* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

藉由結合一或多個 [**D3DXU加值稅LAS**](./d3dxuvatlas.md) 旗標來指定所產生的圖表品質。

</dd> <dt>

*ppMeshOut* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)\***

使用塔 (的已建立網格指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) 。

</dd> <dt>

*pFacePartitioning* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

最終臉部資料分割資料的陣列指標。 每個元素都包含每個臉部一個 DWORD (請參閱 [**ID3DXBuffer**](id3dxbuffer.md)) 。

</dd> <dt>

*ppVertexRemapArray* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

重新對應頂點陣列的指標。 每個陣列元素都會識別原始頂點，也就是當頂點在重新對應) 期間分割時，每個最終頂點的來源 (。 每個陣列元素都包含每個頂點一個 DWORD。

</dd> <dt>

*ppPartitionResultAdjacency* 
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**ID3DXBuffer**](id3dxbuffer.md)介面指標的位址。 此緩衝區將包含每個臉部的三個 Dword 陣列，以針對輸出網格中的每個臉部指定三個相鄰專案。 這個參數不能是 **Null**，因為後續呼叫 D3DXUVAtlasPack () 需要它。

</dd> <dt>

*pfMaxStretchOut* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

由塔演算法產生的最大延展值指標。 範圍介於0.0 到1.0 之間。

</dd> <dt>

*pdwNumChartsOut* \[擴展\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

塔演算法所建立的圖表數目指標。 如果 dwMaxChartNumber 太低，此參數將會傳回建立塔所需的最小圖表數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D 正常」， \_ 否則值為 D3DERR \_ INVALIDCALL。

## <a name="remarks"></a>備註

D3DXUVAtlasPartition 與 [**D3DXUVAtlasCreate**](d3dxuvatlascreate.md)類似，不同之處在于 D3DXUVAtlasPartition 不會執行最終的封裝步驟。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[UVAtlas 函式](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[UV Command-Line 工具 (uvatlas.exe) ](https://msdn.microsoft.com/library/Ee419017(v=VS.85).aspx)
</dt> </dl>

 

 
