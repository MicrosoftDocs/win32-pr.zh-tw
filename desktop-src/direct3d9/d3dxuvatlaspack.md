---
description: Pack 網狀將資料分割成塔。
ms.assetid: 4da85626-c36c-44d9-990b-0db80ed04423
title: 'D3DXUVAtlasPack 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXUVAtlasPack
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6990d6fbc114c874b31d0035a2415d48161d3065718efce3783a041a2097e96f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749658"
---
# <a name="d3dxuvatlaspack-function"></a>D3DXUVAtlasPack 函式

Pack 網狀將資料分割成塔。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXUVAtlasPack(
  _In_       LPD3DXMESH      pMesh,
  _In_       UINT            dwWidth,
  _In_       UINT            dwHeight,
  _In_       FLOAT           fGutter,
  _In_       DWORD           dwTextureIndex,
       const DWORD           *pdwPartitionResultAdjacency,
  _In_       LPD3DXUVATLASCB pCallback,
  _In_       FLOAT           fCallbackFrequency,
  _In_       LPVOID          pUserContent,
  _In_       DWORD           dwOptions,
  _In_       LPD3DXBUFFER    pFacePartitioning
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXMESH**](id3dxmesh.md)**

輸入網格 (的指標，請參閱 [**ID3DXMesh**](id3dxmesh.md)) ，其中包含用來計算塔的物件幾何。 網格至少必須包含位置資料和2D 材質座標。

</dd> <dt>

*dwWidth* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

材質寬度。

</dd> <dt>

*dwHeight* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

材質高度。

</dd> <dt>

*fGutter* \[在\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)**

塔上兩個圖表之間的最小距離（以材質）。 裝訂邊一律會以寬度調整;因此，如果在512x512 材質上使用2.5 的裝訂邊，則兩個圖表之間的最小距離為 2.5/512.0 材質。

</dd> <dt>

*dwTextureIndex* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

以零為基礎的材質座標索引，識別要使用的材質座標集。

</dd> <dt>

*pdwPartitionResultAdjacency* 
</dt> <dd>

類型： **Const [**DWORD**](../winprog/windows-data-types.md) \***

指標，指向每個臉部的三個 Dword 陣列，為網格中的每個臉部指定三個相鄰專案。 它應該衍生自 [**D3DXUVAtlasPartition**](d3dxuvatlaspartition.md)所傳回的 ppPartitionResultAdjacency。 此值不能是 **Null**，因為 Pack 必須知道資料分割步驟中的圖表剪下的位置，才能找出每個圖表的邊緣。

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

要傳回給回呼函式的 void 指標。

</dd> <dt>

*>dwoptions* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

此選項參數目前為保留。

</dd> <dt>

*pFacePartitioning* \[在\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

[**ID3DXBuffer**](id3dxbuffer.md)的指標，其中包含最終臉部資料分割的陣列。 每個元素都包含每個臉部一個 DWORD。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D 正常」， \_ 否則值為 D3DERR \_ INVALIDCALL。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[UVAtlas 函式](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> </dl>

 

 
