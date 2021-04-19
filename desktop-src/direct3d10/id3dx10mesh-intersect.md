---
description: 判斷光線是否與此網格交集。
ms.assetid: 74565d4a-94e6-4faa-bf70-9c1b35e5e5d8
title: ID3DX10Mesh::Intersect 方法 (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.Intersect
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8ceed03ab21debf61371da9e53b5150d2dc83e4a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986517"
---
# <a name="id3dx10meshintersect-method"></a>ID3DX10Mesh：： Intersect 方法

判斷光線是否與此網格交集。

## <a name="syntax"></a>語法


```C++
HRESULT Intersect(
  [in]  D3DXVECTOR3 *pRayPos,
  [in]  D3DXVECTOR3 *pRayDir,
  [in]  UINT        *pHitCount,
  [in]  UINT        *pFaceIndex,
  [in]  float       *pU,
  [in]  float       *pV,
  [in]  float       *pDist,
  [out] ID3D10Blob  **ppAllHits
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRayPos* \[在\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，指定光線開始的時間點。

</dd> <dt>

*pRayDir* \[在\]
</dt> <dd>

類型： **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***

[**D3DXVECTOR3**](d3d10-d3dxvector3.md)結構的指標，指定光線的方向。

</dd> <dt>

*pHitCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

光線與網格交集的次數。

</dd> <dt>

*pFaceIndex* \[在\]
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)\***

如果 pHit 為 **TRUE**，則為最接近光線原點之臉部的索引值指標。

</dd> <dt>

*pU* \[在\]
</dt> <dd>

類型： **float \***

Barycentric 點擊座標的指標，U。

</dd> <dt>

*pV* \[在\]
</dt> <dd>

類型： **float \***

Barycentric 點擊座標的指標，V。

</dd> <dt>

*pDist* \[在\]
</dt> <dd>

類型： **float \***

光線交集參數距離的指標。

</dd> <dt>

*ppAllHits* \[擴展\]
</dt> <dd>

類型： **[ **ID3D10Blob**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

[**ID3D10Blob 介面**](/windows/win32/api/D3DCommon/nn-d3dcommon-id3d10blob)的指標，其中包含 [**D3DX10 \_ INTERSECT \_ 資訊**](d3dx10-intersect-info.md)結構的陣列。 這是交集測試中發生的所有點擊清單。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。

## <a name="remarks"></a>備註

此 API 提供一種方式來瞭解三角形中和周圍的點，與三角形實際所在的位置無關。 此函式會使用下列方程式傳回結果點： V1 + U (V2-V1) + V (V3-V1) 。

平面 V1V2V3 中的任何點都可由 barycentric 座標 (U，V) 表示。 參數 U 會控制要將多少 V2 加權至結果中，而參數 V 控制要將多少 V3 加權到結果中。 最後， \[ 1 (U + V) 的值會 \] 控制 V1 在結果中的加權量。

Barycentric 座標是一種一般座標形式。 在此內容中，使用 barycentric 座標代表座標系統中的變更。 笛卡兒座標的 true 是 barycentric 座標的 true。

Barycentric 座標會根據三角形的頂點定義三角形內的點。 如需 barycentric 座標的更深入說明，請參閱 [Mathworld 的 Barycentric 座標描述](https://mathworld.wolfram.com/BarycentricCoordinates.html)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3DX10。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D3DX10 .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX 介面](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
