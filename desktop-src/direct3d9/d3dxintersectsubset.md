---
description: 將指定的光線與指定的網格子集相交。 這會提供類似的功能來 D3DXIntersect。
ms.assetid: 4a757b9e-18eb-424e-9f3e-cdf917c23787
title: 'D3DXIntersectSubset 函式 (D3DX9Mesh) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIntersectSubset
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95a987730706f32654aab8f63feed61ae87c4d58d27ccccdaed9767d3303bbf8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460378"
---
# <a name="d3dxintersectsubset-function"></a>D3DXIntersectSubset 函式

將指定的光線與指定的網格子集相交。 這會提供類似的功能來 [**D3DXIntersect**](d3dxintersect.md)。

## <a name="syntax"></a>語法


```C++
HRESULT D3DXIntersectSubset(
  _In_        LPD3DXBASEMESH pMesh,
  _In_        DWORD          AttribId,
  _In_  const D3DXVECTOR3    *pRayPos,
  _In_  const D3DXVECTOR3    *pRayDir,
  _Out_       BOOL           *pHit,
  _Out_       DWORD          *pFaceIndex,
  _Out_       FLOAT          *pU,
  _Out_       FLOAT          *pV,
  _Out_       FLOAT          *pDist,
  _Out_       LPD3DXBUFFER   *ppAllHits,
  _Out_       DWORD          *pCountOfHits
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pMesh* \[在\]
</dt> <dd>

類型： **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**

[**ID3DXBaseMesh**](id3dxbasemesh.md)介面的指標，代表要測試的網格。 網格必須進行屬性排序。

</dd> <dt>

*AttribId* \[在\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

要與交集之子集的屬性識別碼。

</dd> <dt>

*pRayPos* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線開始的時間點。

</dd> <dt>

*pRayDir* \[在\]
</dt> <dd>

Type： **Const [**D3DXVECTOR3**](d3dxvector3.md) \***

[**D3DXVECTOR3**](d3dxvector3.md)結構的指標，指定光線的方向。

</dd> <dt>

*pHit* \[擴展\]
</dt> <dd>

類型： **[ **BOOL**](../winprog/windows-data-types.md)\***

BOOL 的指標。 如果光線與網格上的三角形面相交，此值將會設定為 **TRUE**。 否則，此值會設為 **FALSE**。

</dd> <dt>

*pFaceIndex* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

如果 pHit 為 **TRUE**，則為最接近光線原點之臉部的索引值指標。

</dd> <dt>

*pU* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

Barycentric 點擊座標的指標，U。

</dd> <dt>

*pV* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

Barycentric 點擊座標的指標，V。

</dd> <dt>

*pDist* \[擴展\]
</dt> <dd>

類型： **[ **FLOAT**](../winprog/windows-data-types.md)\***

光線交集參數距離的指標。

</dd> <dt>

*ppAllHits* \[擴展\]
</dt> <dd>

類型： **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

[**D3DXINTERSECTINFO**](d3dxintersectinfo.md)結構的陣列，代表所有的點擊，而不只是最接近的點擊。

</dd> <dt>

*pCountOfHits* \[擴展\]
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)\***

從 ppAllHits 傳回之陣列中的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

如果函式成功，則傳回值為「D3D \_ 正常」。 如果函式失敗，則傳回值可以是下列值： E \_ OUTOFMEMORY。

## <a name="remarks"></a>備註

**D3DXIntersectSubset** 函式可讓您瞭解三角形中和周圍的點，而不受三角形實際位置的影響。 此函式會使用下列方程式傳回結果點： V1 + U (V2-V1) + V (V3-V1) 。

平面 V1V2V3 中的任何點都可由 barycentric 座標 (U，V) 表示。 參數 U 會控制要將多少 V2 加權至結果，而參數 V 控制要將多少 V3 加權到結果中。 最後， \[ 1 (U + V) 的值會 \] 控制 V1 在結果中的加權量。

Barycentric 座標是一種一般座標形式。 在此內容中，使用 barycentric 座標代表座標系統中的變更。 笛卡兒座標的 true 是 barycentric 座標的 true。

Barycentric 座標會根據三角形的頂點定義三角形內的點。 如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX9Mesh。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網格函數](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
