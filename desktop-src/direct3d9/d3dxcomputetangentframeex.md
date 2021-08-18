---
description: 在網格上執行正切框架計算。 會產生正切函數、binormal 和選擇性的一般向量。 藉由群組邊緣和分割頂點，Singularities 會視需要進行處理。
ms.assetid: 15cc46bc-6db6-4e1d-a95e-cd60d2666600
title: 'D3DXComputeTangentFrameEx 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeTangentFrameEx
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d091b7ca243e4833cd6aa36a409fca32069e52a267ec3f588b338777ed34338
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988668"
---
# <a name="d3dxcomputetangentframeex-function"></a>D3DXComputeTangentFrameEx 函式

在網格上執行正切框架計算。 會產生正切函數、binormal 和選擇性的一般向量。 藉由群組邊緣和分割頂點，Singularities 會視需要進行處理。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXComputeTangentFrameEx(
  _In_        ID3DXMesh   *pMesh,
  _In_        DWORD       dwTextureInSemantic,
  _In_        DWORD       dwTextureInIndex,
  _In_        DWORD       dwUPartialOutSemantic,
  _In_        DWORD       dwUPartialOutIndex,
  _In_        DWORD       dwVPartialOutSemantic,
  _In_        DWORD       dwVPartialOutIndex,
  _In_        DWORD       dwNormalOutSemantic,
  _In_        DWORD       dwNormalOutIndex,
  _In_        DWORD       dwOptions,
  _In_  const DWORD       *pdwAdjacency,
  _In_        FLOAT       fPartialEdgeThreshold,
  _In_        FLOAT       fSingularPointThreshold,
  _In_        FLOAT       fNormalEdgeThreshold,
  _Out_       ID3DXMesh   **ppMeshOut,
  _Out_       ID3DXBuffer **ppVertexMapping
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **ID3DXMesh**](id3dxmesh.md)\***

輸入 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標。

</dd> <dt>

*dwTextureInSemantic* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

指定紋理座標輸入語義。 如果 D3DX \_ 預設值，此函式會假設沒有紋理座標，而且除非指定了一般向量計算，否則函數會失敗。

</dd> <dt>

*dwTextureInIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

如果網格具有多個材質座標，請指定要用於正切框架計算的材質座標。 如果為零，則表示網格只有單一材質座標。

</dd> <dt>

*dwUPartialOutSemantic* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

指定類型的輸出語義，通常是 D3DDECLUSAGE 的正切函數，其 \_ 描述將儲存 U 紋理座標的部分衍生。 如果 D3DX \_ 預設值，則不會儲存此部分衍生。

</dd> <dt>

*dwUPartialOutIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

指定要在其上儲存部分導數（與 U 材質座標相關）的語義索引。

</dd> <dt>

*dwVPartialOutSemantic* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

指定 [**D3DDECLUSAGE**](./d3ddeclusage.md) 類型（通常是 D3DDECLUSAGE \_ BINORMAL），以描述與 V 材質座標相關的部分衍生會儲存在哪裡。 如果 D3DX \_ 預設值，則不會儲存此部分衍生。

</dd> <dt>

*dwVPartialOutIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

指定要在其上儲存部分導數與 V 材質座標相關的語義索引。

</dd> <dt>

*dwNormalOutSemantic* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

指定輸出正常語義（通常是 D3DDECLUSAGE \_ normal），描述每個頂點的一般向量將儲存在哪個位置。 如果 D3DX \_ 預設值，則不會儲存這個一般向量。

</dd> <dt>

*dwNormalOutIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

指定要在每個頂點上儲存一般向量的語義索引。

</dd> <dt>

*>dwoptions* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

一或多個 [**D3DXTANGENT**](./d3dxtangent.md) 旗標的組合，這些旗標會指定正切框架計算選項。 如果是 **Null**，則會指定下列選項：



| 描述                                                                                              | [**D3DXTANGENT**](./d3dxtangent.md) 旗標值                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| 以弧度為單位，以弧度為單位來加權標準向量長度，以弧度為單位，subtended 由兩個邊緣離開頂點。 | &！ ( D3DXTANGENT \_ 權數（ \_ 依 \_ 區域 \| D3DXTANGENT \_ 權數 \_ 等於 ) ）                |
| 從材質座標計算正笛笛卡兒座標 (u，v) 。 請參閱＜備註＞。                   | &！ ( 從 \_ \_ \_ \| \_ \_ \_ V ) D3DXTANGENT 的 U D3DXTANGENT ORTHOGONALIZE |
| 紋理不是以 u 或 v 方向包裝                                                     | &！ ( D3DXTANGENT \_ 包裝 \_ UV )                                                       |
| 相對於材質座標的部分衍生會正規化。                                  | &！ ( D3DXTANGENT 不會將 \_ \_ \_ 部分標準化 )                                      |
| 頂點會依每個三角形的逆時針方向排序。                               | &！ ( D3DXTANGENT \_ 風的 \_ CW )                                                       |
| 使用已存在於輸入網格中的每個頂點一般向量。                                         | &！ ( D3DXTANGENT \_ 計算 \_ 法線 )                                             |



 

如果 \_ \_ \_ 未設定 [就地產生 D3DXTANGENT]，則會複製輸入網格。 因此，原始網格必須有足夠的空間來儲存計算的一般向量和部分衍生的資料。

</dd> <dt>

*pdwAdjacency* \[在\]
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，為網格中的每個臉部指定三個相鄰專案。 此陣列中的位元組數目必須至少有3個 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md) \* sizeof (DWORD) 。

</dd> <dt>

*fPartialEdgeThreshold* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

指定角度的最大余弦值，而這兩個部分衍生的會被視為不相容。 如果相鄰三角形中兩個部分衍生的方向的點乘積小於或等於此臨界值，則會分割這些三角形之間共用的頂點。

</dd> <dt>

*fSingularPointThreshold* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

指定將頂點視為單數的部分衍生的最大幅度。 由於多個三角形在具有附近正切框架的點上是事件，但會將彼此的 (（例如球體) 的頂端）全部取消，而部分衍生的範圍將會降低。 如果量級小於或等於此臨界值，則會針對包含它的每個三角形分割頂點。

</dd> <dt>

*fNormalEdgeThreshold* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

類似于 fPartialEdgeThreshold，指定在兩個法線之間的角度的最大余弦值，該臨界值超過三角形之間共用的頂點將會被分割。 如果兩個法線的點乘積小於臨界值，共用頂點將會分割，形成相鄰三角形之間的固定邊緣。 如果點乘積超過閾值，鄰近三角形將會有其法線插補。

</dd> <dt>

*ppMeshOut* \[擴展\]
</dt> <dd>

類型： **[ **ID3DXMesh**](id3dxmesh.md)\*\***

輸出 [**ID3DXMesh**](id3dxmesh.md) 網格物件的指標位址，此物件會接收計算的正切函數、binormal 和一般向量資料。

</dd> <dt>

*ppVertexMapping* \[擴展\]
</dt> <dd>

類型： **[ **ID3DXBuffer**](id3dxbuffer.md)\*\***

輸出 [**ID3DXBuffer**](id3dxbuffer.md) 緩衝區物件的指標位址，此緩衝區物件會接收由此方法計算的新頂點與原始頂點的對應。 緩衝區是 Dword 陣列，其陣列大小定義為 ppMeshOut 中的頂點數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為 S \_ OK。 如果函式失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

這個函式的簡化版本會以 [**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)的形式提供。

每個頂點上計算的一般向量一律會正規化為具有單位長度。

適用于計算正笛笛卡兒座標的最穩固解決方案，是不要設定 D3DXTANGENT ORTHOGONALIZE 的旗標， \_ \_ \_ 並 \_ 從 V D3DXTANGENT ORTHOGONALIZE，如此一來，就能 \_ \_ 從紋理座標和 v 來計算正向座標。 不過，在此情況下，如果 u 或 v 為零，則函式會 \_ \_ 分別使用 \_ v 或 D3DXTANGENT \_ ORTHOGONALIZE \_ 中 \_ 的 D3DXTANGENT ORTHOGONALIZE 計算正向座標。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXComputeTangentFrame**](d3dxcomputetangentframe.md)
</dt> </dl>

 

 
